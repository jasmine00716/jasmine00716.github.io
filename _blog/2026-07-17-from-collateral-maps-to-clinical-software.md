---
title: "From Collateral Maps to Clinical Software: What Changed My Research Questions"
date: 2026-07-17
permalink: /blog/from-collateral-maps-to-clinical-software/
excerpt: "Reflecting on how translating stroke-imaging research into MRI and CT medical-device software changed the questions I ask of a model."
tags:
  - Stroke Imaging
  - Clinical AI
  - Research Reflections
---

During my master's research, I developed [3D-MoReT](/portfolio/3d-moret/) to generate multiphase collateral maps from 4D MR perfusion imaging. The research question was relatively well defined: could a lightweight model produce useful maps from a demanding imaging input? At DeepClue, I worked on a different part of the same journey—turning collateral imaging research into MRI and CT software intended for clinical use.

My responsibilities included the MRI image-processing pipeline, application design, verification, documentation, and coordination around hospital deployment. Working across these layers changed what I want to ask before calling a medical AI system successful.

## The input pipeline is part of the system

A paper can describe an input as “an MR perfusion study,” but software receives image files and metadata shaped by acquisition settings. Preprocessing determines which data reach the model and whether the output still corresponds to the intended anatomy and time points. A convincing evaluation therefore needs to examine the complete path from an incoming study to the displayed result, including cases the pipeline cannot process confidently.

This has made me more interested in data quality and failure detection. I want to know how a system behaves when an acquisition differs from the training data, when a series is incomplete, or when preprocessing assumptions no longer hold. These are research questions about robustness as much as they are engineering questions.

## The output needs a clinical purpose

A collateral map can be visually plausible and still leave open the question of how it helps a clinician. Which decision is it meant to support? What information must be visible alongside it? How should uncertainty or an unusable input be communicated? These questions affect what we measure. Numerical scores matter, but they cannot alone tell us whether an output is reliable when someone uses it.

## Verification changes the research agenda

Working on software verification taught me to think in terms of traceable behavior: what the system is expected to do, how that behavior is tested, and what happens outside the expected conditions. For future research, I am especially interested in evaluations that connect model performance with cross-site robustness, workflow constraints, and clinically meaningful failure modes.

My next questions are about multimodal medical imaging and foundation models. I want to study representations that transfer across modalities and tasks, while keeping the full clinical system in view. Translating research into software has made the connection between representation learning and practical validation central to the work I hope to do next.
