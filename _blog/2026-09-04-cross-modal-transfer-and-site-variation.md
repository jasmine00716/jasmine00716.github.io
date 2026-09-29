---
title: "Does Cross-Modal Transfer Survive Hospital-to-Hospital Variation?"
date: 2026-09-04
permalink: /blog/cross-modal-transfer-and-site-variation/
excerpt: "PathoROB raises a question for pathology-to-radiology transfer: do learned representations remain useful when hospitals and acquisition methods change?"
tags:
  - Cross-Modal Learning
  - Foundation Models
  - Domain Shift
---

## Papers and context

[Towards Robust Foundation Models for Digital Pathology](https://www.nature.com/articles/s41467-026-73923-2) — Kömen et al., *Nature Communications*, 2026

[From Pathology to Radiology: Evaluating the Applicability of Pathology Foundation Models](https://doi.org/10.1007/978-3-032-07845-2_4) — Yang, Jung, and Kwak, *MedAGI 2025*

## What PathoROB examines

A representation can contain useful information about tissue and still encode details of where or how an image was acquired. PathoROB evaluates 20 pathology foundation models for sensitivity to non-biological variation across medical centers. The authors examine both the representation space and downstream uses, including prediction, retrieval, and clustering. They find robustness problems across all evaluated models, although the size of the problem varies. The methods they examine reduce these effects but do not eliminate them.

This matters because a high score on one downstream dataset does not reveal which visual features a model relied on. If a diagnosis is correlated with the hospital where images were collected, a model may look transferable for the wrong reason.

## Connection to PathRadX

I contributed to [PathRadX](/portfolio/pathradx/), a study of whether a pathology-pretrained foundation model could support radiology classification without end-to-end fine-tuning. We compared input adaptation and classification strategies on MURA, RSNA Pneumonia, and MedFMC. That work made cross-modal transfer a concrete question for me: which features learned in pathology remain useful for radiology despite differences in appearance and task?

PathoROB asks a different question. It studies robustness **within digital pathology**, not pathology-to-radiology transfer. Its findings therefore cannot be treated as a direct result about PathRadX. They do suggest a useful next test: when a frozen encoder transfers across modalities, how much of its apparent value remains after hospital, device, and acquisition differences are separated from the clinical labels?

## An evaluation I would like to see

I would compare transfer under patient-level and institution-level splits, report performance separately by acquisition source where possible, and examine whether feature embeddings cluster by diagnosis or by site. I would also test whether a simple adaptation changes the dependence on site-specific cues, rather than judging it only by average accuracy.

## Takeaway

Cross-modal transfer is most compelling when it survives changes in both **what is imaged** and **how the image was produced**. PathoROB reinforces my interest in representations that remain useful across institutions and acquisition protocols.
