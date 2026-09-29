---
title: "Segment Anything: Promptable Segmentation Meets Medical Imaging"
date: 2024-05-24
permalink: /blog/segment-anything/
excerpt: "SAM reframes segmentation as a promptable task, but clinical use still depends on domain adaptation, uncertainty, and workflow design."
tags:
  - Segment Anything
  - Foundation Models
  - Medical Image Segmentation
---

## Paper

[Segment Anything](https://openaccess.thecvf.com/content/ICCV2023/html/Kirillov_Segment_Anything_ICCV_2023_paper.html) — Kirillov et al., ICCV 2023

## Core idea

Segment Anything Model (SAM) reframes segmentation as a promptable task. An image encoder computes a reusable image representation, a prompt encoder represents points, boxes, or masks, and a lightweight mask decoder produces candidate segmentations. This separation allows the same image embedding to support repeated interactive prompts.

The model is paired with SA-1B, a dataset containing more than one billion masks from 11 million images. The data engine and promptable objective are as important as the architecture: they are intended to make a single model useful across objects and image distributions without task-specific retraining.

## Why it mattered

SAM changes the expected interface to a segmentation system. Instead of training a separate model for every label set, a user specifies the target at inference time. This makes segmentation useful as an interactive tool and as an annotation accelerator, even when the desired object category was not explicitly defined during training.

The promptable design also changes how generalization is tested: a target can be specified at inference time rather than being limited to categories fixed during training.

## Medical imaging perspective

The interaction model is attractive for clinical annotation. A radiologist could provide a point or bounding box and refine a mask, potentially reducing the effort required to create training data or quantitative measurements.

However, “anything” should be interpreted cautiously in medicine. SAM was trained primarily on natural images, while medical images differ in intensity distribution, texture, resolution, and semantics. Many clinical targets have weak boundaries, low contrast, or no natural-object equivalent. A bounding box around a lesion can also provide substantial prior information, so box-prompt performance should not be confused with fully automatic detection and segmentation.

Many CT and MR studies are volumetric, whereas the original SAM operates on 2D images. Processing slices independently may produce discontinuous masks and ignore voxel spacing. Clinical use also calls for uncertainty estimates, reproducibility, failure detection, and validation across sites—properties that impressive visual examples do not establish on their own.

## Takeaway

SAM is most convincing to me as an interactive segmentation interface. Its promptable design can support annotation and clinician-guided workflows, while medical deployment requires domain-specific adaptation and evaluation. The practical test is whether it reduces work while allowing users to catch clinically meaningful errors.
