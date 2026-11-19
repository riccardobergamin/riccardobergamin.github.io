---
layout: page
title: Possession Risk Estimate from Spatio-temporal State (PRESS)
description: A physics-informed framework for studying defensive pressure and possession vulnerability in football
img: assets/img/press_logo.png
importance: 1
category: football-analytics
related_publications: false
github: https://github.com/riccardobergamin/PRESS
---

## Overview

Defensive pressure in football emerges from collective interactions between players, shaping the space available to the ball carrier, the feasibility of passing and carrying, and the difficulty of retaining possession.

PRESS (Possession Risk Estimate from Spatio-temporal State) is an independent, physics-informed research and software framework that uses tracking and event data to quantify possession vulnerability. It explores alternative formulations of Expected Possession Value (EPV) components, with particular interest in how players experience, respond to, and overcome defensive pressure.

## Approach

PRESS builds on the Markov decision process formulation and modular architecture of EPV models, combining physics-based models of passing and ball carrying with statistical models of player decisions and possession outcomes.

The framework estimates two complementary quantities: **possession-loss hazard**, the probability of losing team possession during the next action, and **xLoss**, the probability that the current ball carrier's individual possession eventually ends in a loss, following SkillCorner's definition.

<div class="row mt-3 justify-content-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid
            path="assets/img/press_tracking.png"
            class="img-fluid rounded z-depth-1"
        %}
    </div>
</div>
<div class="caption">
    Example of a game situation reconstructed from tracking data.
    Player positions and movement provide the basis for modelling
    action feasibility, spatial opportunities, and possession-loss risk.
</div>

## Methodological contributions

PRESS investigates a physics-based formulation of **ball-drive risk**, modelling the probability of losing possession through the relative movement and interception capabilities of defenders and the ball carrier.

The framework also develops a competing-risks formulation of **Ball Carrier Open Space (BCOS)**, providing a probabilistic representation of the space potentially accessible to the carrier under defensive opposition. Physics-derived features are incorporated into statistical models of action selection, pass destination choice, and possession outcomes. To the best of my knowledge, multinomial gradient-boosted trees had not previously been applied to pass selection, and xLoss is computed modularly as the hazard plus a residual-risk term.

A further component is the interpretation of possession-loss risk through **discrete-time survival analysis**. PRESS uses possession half-life to define interpretable difficulty bands and examines how hazard evolves throughout observed possessions.

Individual components are evaluated through dedicated benchmarks, with comparisons to existing football analytics approaches whenever feasible.

## Applications

Following SkillCorner's pressure metrics, PRESS supports the retrospective characterization of player behaviour under defensive pressure. Risk trajectories allow the identification of recurring pressure patterns, contributing to player profiles that describe how individuals encounter and respond to defensive constraints.

Comparing observed possession outcomes with model-based expectations across difficulty levels provides a complementary assessment of player performance. The framework also supports prospective analysis of possession vulnerability and tactical situations through xLoss.

## My contribution

**Independent research and software development**

I designed the modelling framework and validation protocols and developed the core software architecture.

Physics-based modelling · Probabilistic modelling · Machine learning · Scientific software development · Football analytics

## Code & repository

PRESS is implemented as a modular Python package, with methodological tutorials, benchmark analyses, documented research workflows, and reproducible examples based on real match data.

The project uses the publicly available ten-match SkillCorner A-League sample as its primary dataset and includes workflows for applying the framework to tracking data from other providers. The limited sample constrains the generalizability of the fitted models and empirical findings.

The code is available on [GitHub](https://github.com/riccardobergamin/PRESS), with full documentation and examples on the [project website](https://riccardobergamin.github.io/PRESS/).

## Project status

Ongoing exploratory research and software development.