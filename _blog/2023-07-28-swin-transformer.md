---
title: "Swin Transformer: A Practical Bridge Between CNN Hierarchies and Attention"
date: 2023-07-28
permalink: /blog/swin-transformer/
excerpt: "Why shifted-window attention made Transformers more practical for high-resolution images and dense prediction tasks."
tags:
  - Swin Transformer
  - Computer Vision
  - Medical Imaging
---

## Paper

[Swin Transformer: Hierarchical Vision Transformer Using Shifted Windows](https://openaccess.thecvf.com/content/ICCV2021/html/Liu_Swin_Transformer_Hierarchical_Vision_Transformer_Using_Shifted_Windows_ICCV_2021_paper.html) — Liu et al., ICCV 2021

## Core idea

The original ViT produces a single-scale sequence and applies global self-attention, which becomes expensive as image resolution increases. Swin Transformer changes both properties. It builds a hierarchy by progressively merging neighboring patches, and it computes self-attention only within local windows.

Local windows alone would isolate neighboring regions from one another. Swin addresses this by alternating regular and shifted window partitions. Tokens grouped into separate windows in one block can interact in the next block, allowing information to move across window boundaries while keeping computation approximately linear in the number of image patches.

## Why it mattered

This design makes the Transformer look more like a general-purpose vision backbone. The hierarchy produces multi-scale feature maps, which are natural inputs to detection and segmentation heads. The local-window constraint also makes high-resolution processing more manageable than full global attention.

What I find most useful is the compromise. Swin does not frame locality as something that must be eliminated. Instead, it uses local computation for efficiency and gradually expands the effective receptive field through depth and shifting. This is closer to the practical requirements of dense prediction than a uniform sequence processed globally at every layer.

## Medical imaging perspective

The architecture maps naturally to 3D medical images: patches can become volumes, windows can operate locally in three dimensions, and hierarchical features can support encoder–decoder segmentation models. Local attention is particularly important because a CT or MR volume can generate far more tokens than a 2D natural image.

However, windowing also introduces choices that should not be treated as implementation details. A lesion or vascular structure may cross a window boundary. Anisotropic voxel spacing means that a cubic window in index space may not represent a cubic region anatomically. Patch size, window size, and downsampling schedule should therefore reflect both the target anatomy and the acquisition protocol.

Swin also does not make attention globally cheap in a single step. Long-range interaction emerges across successive shifted-window blocks. Whether that is sufficient depends on the depth of the network and the spatial relationships required by the task.

## Takeaway

Swin Transformer is compelling because it turns attention into a usable multi-scale backbone. For medical imaging, its value is not simply that it is a Transformer; it is that the architecture exposes a workable balance among local detail, cross-region communication, and memory cost.
