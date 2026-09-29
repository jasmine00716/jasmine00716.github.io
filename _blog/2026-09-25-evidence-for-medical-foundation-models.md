---
title: "What Evidence Would Convince Me to Use a Medical Foundation Model?"
date: 2026-09-25
permalink: /blog/evidence-for-medical-foundation-models/
excerpt: "CLEAR and REAL-FM prompt a practical evaluation question: can we explain a medical model's decisions and show that it works in the setting where it will be used?"
tags:
  - Clinical AI
  - Foundation Models
  - Model Evaluation
---

## Papers

[CLEAR: An Auditable Foundation Model for Radiology Grounded in Clinical Concepts](https://www.nature.com/articles/s41551-026-01741-4) — Han et al., *Nature Biomedical Engineering*, 2026

[Foundation Models in Biomedical Imaging: Turning Hype into Reality](https://www.nature.com/articles/s41551-026-01762-z) — Muneer et al., *Nature Biomedical Engineering*, 2026 (Perspective)

## Two different kinds of evidence

CLEAR approaches chest X-ray interpretation through radiological concepts extracted from image–report pairs. Its predictions can be examined in terms of contributing observations, and the authors use that structure to investigate confounding patterns and test the model on external datasets. I find the auditing idea valuable: when performance changes, we should be able to ask *which concepts contributed to a prediction*, not only whether its score fell.

In their REAL-FM Perspective, Muneer and colleagues ask a wider question. They propose evaluating foundation models in terms of data, technical readiness, clinical value, workflow integration, and responsible AI. A model may perform well on a benchmark and still be difficult to trust or use in a clinical setting. The framework puts those practical questions in the evaluation plan from the start.

## My proposed evidence checklist

First, I would want evidence that the input and target match the intended use. This includes how studies are selected, how labels are defined, and how incomplete or low-quality acquisitions are handled. A result on a curated dataset cannot by itself establish behavior on routine studies.

Second, I would ask for performance across sites and relevant patient groups, with failure cases reported alongside average metrics. For a model that produces a map or segmentation, I would examine the spatial pattern and its clinical consequences, not only an aggregate overlap or error score. For a classification model, I would look at calibration and the consequences of different operating thresholds.

Third, I would want a way to investigate *why* the system failed. CLEAR illustrates one approach by exposing concept-level contributions. An explanation is useful only if it helps identify a problem or supports a meaningful check; a plausible-looking explanation is not proof that the prediction is correct.

Finally, I would test the full workflow. Who sees the output? How long does it take to appear? What happens when the system cannot produce a trustworthy result? Does it help with the clinical task it was designed for? My experience building stroke-imaging software makes these questions inseparable from model evaluation.

## Takeaway

For me, a convincing medical foundation model needs more than a strong benchmark result. It needs evidence about generalization, inspectable failures, and value in the intended workflow. CLEAR provides an example of how model decisions can be audited; REAL-FM provides a broader lens for judging whether that capability is enough in practice.
