---
title: "NeuroVFM: What Can a Model Learn from Routine Brain Scans?"
date: 2026-10-13
permalink: /blog/neurovfm-learning-from-routine-neuroimaging/
excerpt: "NeuroVFM learns from millions of clinical CT and MRI volumes. I look at its 3D self-supervised objective, diagnostic evaluation, and the questions that remain for stroke imaging."
tags:
  - Neuroimaging
  - 3D Medical Imaging
  - Foundation Models
---

## Paper

[Health system learning enables generalist neuroimaging models](https://www.nature.com/articles/s41591-026-04497-1) — Kondepudi et al., *Nature Medicine*, July 2026

## What the model learns

NeuroVFM starts from an unusually broad clinical imaging archive: 5.24 million CT and MRI volumes from 566,915 studies at one health system. Its visual encoder is pretrained without diagnosis labels or report text. Instead, the authors use Vol-JEPA, a 3D self-supervised method that asks a model to predict the latent representation of hidden regions from visible parts of a volume. The target is a learned representation, rather than the missing pixels themselves.

That distinction matters to me after reading about [masked autoencoders](/blog/masked-autoencoders/). Both approaches learn from partially visible images, but NeuroVFM emphasizes prediction in feature space and trains directly on heterogeneous clinical volumes. It also learns a shared visual representation for CT and MRI. Diagnostic labels extracted from radiology reports enter later, when the authors evaluate and adapt that representation for specific tasks; they are not the pretraining target.

## What the evaluation shows

The authors evaluate diagnosis across 82 CT and 74 MRI categories using a temporally held-out set of more than 50,000 studies from the same health system. They also test transfer on public neuroimaging benchmarks. Their results suggest that learning from routine clinical volumes can produce more useful neuroimaging features than the general-purpose and medical-image baselines in these comparisons.

The paper goes beyond classification. A frozen NeuroVFM encoder is connected to a language model to generate preliminary findings from imaging studies. The authors then evaluate report quality and triage on an expert-reviewed set of 300 CT and MRI studies. I find the separation between a domain-trained visual encoder and a language model especially interesting: it gives a concrete way to ask whether the system's clinical statements are grounded in image features.

## Questions for stroke imaging

My work on [3D-MoReT](/portfolio/3d-moret/) involved dynamic MR perfusion and collateral maps, where the output depends on spatial detail and changes over time. NeuroVFM's strong study-level results do not establish how well its features would support voxel-level maps, vessel detail, or perfusion dynamics. I would test those tasks separately, with attention to how the paper's resampling and intensity processing affect subtle findings.

I would also want external validation across hospitals. The study includes public benchmark tests and a large temporal holdout, but its main clinical archive comes from one health system. Report-derived diagnostic labels are useful at scale, yet they are an imperfect reference for every case. Prospective workflow evaluation and uncertainty reporting would be important before relying on generated findings for clinical decisions.

## Takeaway

NeuroVFM makes a persuasive case for learning directly from the CT and MRI studies hospitals already collect. For my research, its most useful lesson is methodological: pretrain on the diversity of real clinical volumes, then test whether that representation transfers to the *specific* spatial and temporal outputs a stroke-imaging task requires.
