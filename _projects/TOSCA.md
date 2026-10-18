---
layout: page
title: Bayesian Timing of Somatic Events in Cancer (TOSCA)
description: A framework to infer the timing of drug-resistant clones in individual cancer patients
img: assets/img/tosca.png
importance: 2
category: cancer-evolution
related_publications: false
github: https://github.com/caravagnalab/TOSCA
---

## Overview

Cancer evolution is shaped by genetic alterations that accumulate over years of tumour growth and treatment. While genome sequencing can identify the mutations present in a tumour, it generally cannot determine when those alterations arose, making it difficult to distinguish pre-existing resistance from adaptations acquired during therapy.

TOSCA (Timing of Somatic Events in Cancer) is a Bayesian framework that reconstructs the timing of clonal expansions in individual patients using longitudinal whole-genome sequencing data.

## Approach

TOSCA combines longitudinal genomic data with treatment history and multiple molecular clocks derived from somatic mutations to probabilistically map genomic events onto the clinical timeline of a patient.

The framework models cancer evolution as a stochastic process and reconstructs the temporal order of different somatic events, including copy-number alterations, whole-genome doubling, and point mutations. It also accounts for tumour dormancy and treatment-associated evolutionary dynamics.

## Key findings

TOSCA was validated by recovering established developmental dynamics in childhood neuroblastoma, including the early acquisition of aneuploidy during embryogenesis followed by the accumulation of segmental chromosomal alterations.

We further applied the framework to haematological and solid malignancies exposed to chemotherapy, immunotherapy, and stem-cell transplantation. Across these settings, TOSCA reconstructed the timing of clonal expansions associated with copy-number and point mutations.

Importantly, TOSCA distinguished resistant clones that predated treatment from those that emerged afterwards, providing a way to determine the temporal relationship between tumour evolution and therapy.

## Impact

By linking evolutionary histories to treatment records, TOSCA provides a framework for studying cancer evolution and the origin of therapeutic resistance at the level of individual patients.

The framework enables genomic alterations to be placed within their temporal and clinical context, providing a quantitative approach to understanding how treatment shapes cancer evolution.

## My contribution

**Joint first author**

Framework development · Bayesian modelling · Mathematical modelling · Computational cancer evolution

## Code & repository

The code and examples are available on [GitHub](https://github.com/caravagnalab/TOSCA).

## Publication status

Manuscript under review at *Nature Genetics*.
