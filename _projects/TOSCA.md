---
layout: page
title: Bayesian Timing of Somatic Events in Cancer (TOSCA)
description: A framework to infer the timing of drug-resistant clones in individual cancer patients
img: assets/img/tosca.png
importance: 1
category: work
related_publications: false
github: https://github.com/caravagnalab/TOSCA
---

We developed TOSCA (Timing of Somatic Events in Cancer), a Bayesian framework that leverages longitudinal whole-genome sequencing data to determine whether drug resistance arises from pre-existing clones or is acquired after treatment.  

Key features and novelty:  
- Integrates treatment timing, duration, and tumour molecular features into a point process model augmented with population genetics.  
- Estimates the origin time of drug-resistant clones from pre-treatment and relapse samples.  
- Handles different types of genetic events, including copy-number alterations, whole-genome doubling, and mutations affecting mutation rates.  
- Models stochastic dormancy to capture the impact of chemotherapy on mutation accumulation.  
- First approach to time evolution in a single patient, accounting for treatment-associated evolution and avoiding confounding from tumour heterogeneity.  

The code and examples are available on [GitHub](https://github.com/caravagnalab/TOSCA).

