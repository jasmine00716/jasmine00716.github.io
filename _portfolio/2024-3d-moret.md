---
title: "3D-MoReT: Collateral Imaging from 4D MR Perfusion"
collection: portfolio
permalink: /portfolio/3d-moret/
date: 2024-07-13
period: "2023–2024"
venue: "Korea University · CARS 2024"
role: "First Author & Lead Researcher"
summary: "Developed a lightweight 3D CNN–Transformer regression model that generates five-phase collateral maps directly from 4D DSC-MR perfusion imaging."
highlight: "Evaluated on 952 patients from two university hospitals; the model outperformed similarly sized networks and matched substantially heavier baselines."
links:
  - label: "GitHub"
    url: "https://github.com/jasmine00716/3D-MoReT"
  - label: "Paper"
    url: "https://doi.org/10.1007/s11548-024-03229-5"
technologies:
  - PyTorch
  - 3D CNN
  - Vision Transformer
  - DSC-MRP
  - Regression
---

## Overview

3D-MoReT generates five-phase collateral maps directly from 4D dynamic susceptibility contrast MR perfusion images. The model combines efficient convolutional feature extraction with Transformer-based global representation learning.

![Overview of the 3D-MoReT architecture](/images/timeline/3d-moret-architecture.png)

## My Contributions

- Led the study from problem formulation and preprocessing through model design, implementation, experiments, comparative analysis, and initial manuscript drafting.
- Designed a 3D CNN–Transformer regression model combining MobileNetV2, MobileViT, ViT, and residual and skip connections.
- Built the training and evaluation pipeline for multi-institutional 4D DSC-MRP data.
- Evaluated the model on 952 patients from two university hospitals.

## Outcome

The proposed model outperformed similarly sized approaches and achieved performance comparable to substantially heavier baselines. The work was published in the *International Journal of Computer Assisted Radiology and Surgery* and presented at CARS 2024.

[View the code](https://github.com/jasmine00716/3D-MoReT) · [Read the paper](https://doi.org/10.1007/s11548-024-03229-5)
