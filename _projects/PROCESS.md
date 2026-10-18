---
layout: page
title: "SCOUT: Synthetic Cancer Genomes for Evolutionary Benchmarking"
description: A synthetic whole-genome sequencing resource for benchmarking tumour genomic analysis and evolutionary inference
img: assets/img/scout.png
importance: 4
category: cancer-evolution
related_publications: false
---

## Overview

Cancer genomes are shaped by evolutionary processes linking mutagenesis, clonal selection, spatial growth, and treatment response. However, benchmarking strategies for tumour genomic analysis often lack a controlled evolutionary ground truth.

SCOUT is a large-scale synthetic whole-genome sequencing resource designed to benchmark tumour genomic analysis and evolutionary inference under controlled evolutionary ground truth.

The resource comprises more than 200 synthetic tumour samples and recapitulates key features of solid and haematological malignancies, including driver mutations, chromosomal instability, complex mutational processes, intratumour heterogeneity, spatial sampling, and treatment-associated evolutionary dynamics.

## Approach

SCOUT uses synthetic tumour and matched-normal whole-genome sequencing data with longitudinal and multi-region sampling to provide a controlled ground truth for evaluating genomic analysis methods.

We used SCOUT to benchmark widely used approaches for somatic variant detection, copy-number analysis, mutational signature inference, and tumour evolutionary inference.

## Key findings

Performance deteriorated in low-purity, highly subclonal, and structurally complex tumours across multiple analytical tasks.

Spatial sampling bias and hypermutation generated spurious evolutionary signals that could confound the interpretation of tumour evolution.

Tumour purity consistently had a stronger effect on inference accuracy than sequencing depth, highlighting the importance of evolutionary and biological complexity when evaluating genomic analysis methods.

## Impact

SCOUT establishes evolutionary ground truth as a prerequisite for reproducible benchmarking and interpretation of whole-genome sequencing data in cancer genomics.

The resource provides a controlled framework for evaluating computational methods under realistic evolutionary scenarios that are difficult to reproduce in real tumour datasets.

## My contribution

**Joint last author**

Co-supervision of SCOUT development · Cancer evolution · Computational benchmarking · Evolutionary inference

## Resource & documentation

The SCOUT resource and documentation are available through the ProCESS project:

[SCOUT documentation ↗](https://caravagnalab.github.io/ProCESS/latest/articles/ProCESS.html)

## Related work

**Preprint — 2026**

[View preprint ↗](https://www.biorxiv.org/content/10.64898/2026.06.09.731105v1)

Publication status

Manuscript under review at *Nature Communications*.
