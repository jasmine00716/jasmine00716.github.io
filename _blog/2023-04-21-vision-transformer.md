---
title: "Vision Transformer: What Changes When Images Become Token Sequences?"
date: 2023-04-21
permalink: /blog/vision-transformer/
excerpt: "A reading note on ViT, its deliberately minimal architecture, and the trade-off between global modeling and data efficiency in medical imaging."
tags:
  - Vision Transformer
  - Computer Vision
  - Medical Imaging
---

## Paper

[An Image Is Worth 16×16 Words: Transformers for Image Recognition at Scale](https://openreview.net/forum?id=YicbFdNTTy) — Dosovitskiy et al., ICLR 2021

## Core idea

The most striking part of the Vision Transformer (ViT) is not a complicated new attention mechanism. It is the decision to treat an image as a sequence with as few vision-specific assumptions as possible. The image is divided into fixed-size patches, each patch is projected into an embedding, positional information is added, and the resulting sequence is processed by a standard Transformer encoder. A learnable class token collects the representation used for classification.

This formulation replaces the locality and translation-equivariance built into convolution with learned relationships among patches. With sufficiently large-scale pre-training, the model can discover useful visual structure rather than having that structure prescribed by the architecture.

## Why it mattered

ViT showed that the Transformer could be a primary visual backbone, not merely an auxiliary module attached to a CNN. Its simplicity also made the paper influential: later work could improve data efficiency, introduce hierarchical representations, or extend attention to dense prediction without abandoning the patch-token formulation.

The result comes with an important qualification. ViT becomes especially competitive when trained on large datasets. On smaller datasets, the weaker inductive bias can be a disadvantage. The paper therefore reads not only as an architectural proposal but also as an argument about scale: model design, pre-training data, and transfer learning have to be considered together.

## Medical imaging perspective

Global context is attractive in medical imaging. A local abnormality may need to be interpreted relative to the contralateral anatomy, the surrounding vascular territory, or a pattern distributed across multiple regions. Attention offers a direct mechanism for relating distant patches.

At the same time, medical datasets are usually much smaller than natural-image pre-training corpora. Image resolution can be high, and volumetric data makes the token count grow quickly. Converting a 3D scan into small tokens may preserve detail but make global attention prohibitively expensive; using large tokens reduces the cost but risks losing small lesions and fine boundaries.

Another concern is what the model learns during transfer. A representation that works well for natural-image classification may not encode acquisition physics, intensity meaning, or subtle pathological changes in MR and CT. Pre-training helps, but the source data and objective still matter.

## Takeaway

ViT is useful as a clean reference point: it asks how far a model can go when an image is treated as a token sequence. For medical imaging, the answer is promising but conditional. Global modeling is valuable, yet the architecture must still respect limited labels, volumetric computation, resolution, and modality-specific information.
