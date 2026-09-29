---
title: "When Is a 3D Model Worth the Cost?"
date: 2026-08-07
permalink: /blog/when-is-a-3d-model-worth-the-cost/
excerpt: "A CVPR 2026 study of 2D foundation models for 3D classification prompts a closer look at which medical-imaging tasks truly need volumetric reasoning."
tags:
  - 3D Medical Imaging
  - Foundation Models
  - Model Efficiency
---

## Paper

[Revisiting 2D Foundation Models for Scalable 3D Medical Image Classification](https://openaccess.thecvf.com/content/CVPR2026/html/Liu_Revisiting_2D_Foundation_Models_for_Scalable_3D_Medical_Image_Classification_CVPR_2026_paper.html) — Liu et al., *CVPR*, 2026

## Core idea

CT and MRI scans are often volumetric, but a 3D input does not automatically require a 3D encoder. Liu and colleagues introduce AnyMC3D, which adapts a frozen 2D foundation-model backbone to 3D classification through lightweight, task-specific components. It extracts information from slices and combines it for a volume-level prediction. The paper evaluates methods across 12 classification tasks involving different anatomies, pathologies, and imaging modalities.

The authors report that well-adapted 2D foundation models outperform the 3D architectures they benchmark for these classification tasks. Their result is a useful challenge to choosing an architecture simply because its input has three spatial dimensions.

## How I read the result

The comparison highlights how much depends on the *adaptation strategy*. A strong pretrained 2D representation can be valuable if the model combines evidence across slices effectively and learns what is specific to the new task. Model size alone is a poor proxy for useful capacity: a lightweight adaptation may make better use of a pretrained backbone than a larger 3D model trained with limited medical data.

At the same time, the paper's conclusion is about **volume-level classification**. It should not be read as evidence that slice aggregation is sufficient for every volumetric task. My [3D-MoReT](/portfolio/3d-moret/) project generated five-phase collateral maps from 4D MR perfusion data. That problem asks for spatially structured outputs and clinically relevant temporal information, not only one label per volume. The need to preserve correspondence across space and time changes the architectural trade-off.

## Questions I would test next

For a new task, I would first ask what information the target actually requires. Can a decision be made from a few informative slices, or does it depend on relationships between neighboring regions? Is the output a class label, a lesion mask, a quantitative map, or a time-resolved image? Those distinctions should guide a comparison between slice-based, 2.5D, and native 3D approaches.

I would also compare more than a single headline score: training data requirements, inference time, memory use, cross-hospital performance, and the quality of localization or dense outputs. For clinically deployed software, these costs and failure modes are part of the model choice.

## Takeaway

The paper makes a strong case for testing carefully adapted 2D foundation models before assuming that a 3D backbone is necessary for classification. My broader takeaway is to match the representation to the *task and output*, then evaluate whether extra spatial modeling earns its computational cost.
