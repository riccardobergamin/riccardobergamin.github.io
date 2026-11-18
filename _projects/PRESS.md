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

Defensive pressure in football emerges from the collective interactions between players, shaping the space available to the ball carrier, the feasibility of passing and carrying, and the difficulty of retaining possession.

PRESS (Possession Risk Estimate from Spatio-temporal State) is a physics-informed framework that combines event and tracking data to study defensive pressure through the risk of losing possession.

PRESS was developed as a personal portfolio project to gain hands-on experience with football analytics, develop a deeper understanding of possession valuation methodologies, and translate these concepts into reusable software. The project also provides an opportunity to explore alternative modelling approaches drawing on my background in physics, applied mathematics, and probabilistic inference.

## Approach

PRESS builds on the Markov decision process formulation and modular architecture of Expected Possession Value (EPV) models, adapting this perspective to the study of possession vulnerability.

The framework adopts a hybrid modelling strategy that combines physics-based models of passing and ball carrying with statistical learning models of player decision-making. Physical models characterise the feasibility and risk of available actions, while tree-based models describe how players select actions and pass destinations, incorporating physics-derived features alongside tactical and contextual information.

These components are integrated under a decision-making policy learned from observed play to estimate possession-loss risk at two complementary horizons: the probability of losing team possession during the next action (possession-loss hazard) and the probability that the current ball carrier's individual possession eventually ends in a loss (xLoss).

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

PRESS explores a physics-based formulation of ball-drive success, modelling the probability of retaining possession through the relative movement and interception capabilities of the ball carrier and defenders.

The framework also introduces a competing-risks formulation of Ball Carrier Open Space (BCOS), providing a probabilistic representation of the space potentially accessible to the carrier in the presence of defensive opposition. This representation connects the physical dynamics of player interactions to statistical models of decision-making and possession outcomes.

A further contribution is the interpretation of possession-loss risk through survival analysis. By interpreting the next-action loss probability as a discrete hazard and introducing a reference possession half-life, PRESS defines interpretable possession-difficulty bands for studying defensive pressure.

Each modelling task is developed within a rigorous machine learning workflow, with systematic validation and benchmarking against existing approaches in the football analytics literature whenever possible.

## Impact

By connecting the physical dynamics of player interactions with learned decision-making policies, PRESS provides a quantitative framework for studying possession vulnerability and defensive pressure.

The framework supports tactical analysis and the evaluation of player behaviour under pressure, contextualising individual decision-making and possession retention within the difficulty of the situations faced. This provides a basis for investigating how players manage possession and respond to defensive constraints across different levels of pressure.

## My contribution

**Independent development — Personal portfolio project**

 Physics-based modelling · Probabilistic modelling · Machine learning · Scientific software development · Football analytics

## Code & repository

PRESS is implemented as a modular Python package, with methodological tutorials, benchmark analyses, documented research workflows, and reproducible examples based on real match data.

The project uses the publicly available SkillCorner A-League sample as its primary dataset and includes workflows for applying the framework to tracking data from other providers.

The code is available on [GitHub](https://github.com/riccardobergamin/PRESS), with full documentation and examples on the [project website](https://riccardobergamin.github.io/PRESS/).

## Project status

Ongoing personal portfolio project.
