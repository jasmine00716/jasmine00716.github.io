---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Research Interests
======

Large-scale multimodal and foundation models for medical AI; vision–language learning; medical image analysis; clinical representation learning across institutions, modalities, and tasks.

Education
======

### Korea University, Seoul, Republic of Korea

*M.S. in Computer Engineering, Mar. 2023 – Feb. 2025*

- Advisor: Prof. Jin Tae Kwak
- Selected coursework: Medical Imaging; Efficient AI and Hardware Design; Advanced Digital Signal Processing; Random Signal Analysis

### Dongduk Women's University, Seoul, Republic of Korea

*B.S. in Computer Science, Mar. 2019 – Feb. 2023*


Research Experience
======

### PathRadX: Pathology Foundation Models for Radiology

*Contributing Researcher, DeepClue Inc., 2025*

- Supported data preparation, result analysis, and manuscript drafting for a study evaluating whether a frozen pathology foundation model could transfer to radiology tasks.
- Contributed to experiments spanning MURA, RSNA pneumonia, and MedFMC datasets and comparisons of modality-adaptation and task-classification strategies; collaborators led model design, implementation, and experiment execution.
- Published in the MedAGI 2025 workshop proceedings held with MICCAI 2025.

### ISLES 2024: Multimodal Infarct Segmentation

*Research Design and Analysis, Korea University, 2024*

- Contributed problem definition, data preparation, method and experimental design, comparative analysis, and abstract preparation for a 3D Vision Transformer using NCCT, CTP, CTA, and Tmax inputs.
- Collaborated with a teammate who implemented the code and ran the experiments.

### 3D-MoReT: Collateral Imaging from 4D MR Perfusion

*First Author and Lead Researcher, Korea University, 2023–2024 · [Project and code](https://github.com/jasmine00716/3D-MoReT)*

- Led the study from problem formulation and data preprocessing through model design, implementation, experiments, comparative analysis, and initial manuscript drafting.
- Designed a 3D CNN–Transformer regression model combining MobileNetV2, MobileViT, ViT, and residual/skip connections to generate five-phase collateral maps from 4D DSC-MRP.
- Evaluated the model on 952 patients from two university hospitals; outperformed similarly sized models and matched substantially heavier baselines.
- Published the work as first author in the *International Journal of Computer Assisted Radiology and Surgery* and presented it at CARS 2024.

Industry Experience
======

### DeepClue Inc., Seoul, Republic of Korea

*Team Leader, Engineering & Manufacturing Team, Sep. 2024 – Jun. 2026*

- Led the translation of collateral-imaging research into DeepClue-Precise MRI/CT software as a medical device (SaMD), coordinating clinical requirements, system architecture, implementation, verification, regulatory documentation, and team operations.
- Developed the MRI application and image-processing pipeline end to end, including DICOM preprocessing, image analysis, GUI, output generation, and testing.
- Designed the reusable application framework adopted by the CT product and collaborated with the developer responsible for its CT-specific core image-processing pipeline.
- Designed and executed software verification and validation, prepared regulatory and quality-system documents, coordinated with hospitals and external organizations, and led activities supporting MFDS Class I medical-device registration.
- Supported hospital prototype deployment and converted clinical feedback into software requirements and validation criteria.

Publications
======

- H. J. Ki, H. G. Roh, S. B. Lee, J. T. Kwak, J. J. Park, Y. S. Jeon, **S. Jung**, H. Yang, C. Yu, J. S. Lee, H. J. Lee, and H. J. Kim. “Collateral Perfusion Score for Predicting Futile Endovascular Thrombectomy in Acute Anterior Circulation Stroke.” *Korean Journal of Radiology*. *Under review.*
- H. Kim, H. G. Roh, J. T. Kwak, H. J. Ki, I. S. Kim, **S. Jung**, H. Yang, J. J. Park, Y. S. Jeon, and H. J. Kim. “Simultaneous generation of color-coded arteriography, venography, and dynamic angiography: methodology and clinical applications in stroke.” *La Radiologia Medica*, 130(11):1820–1826, 2025. [doi:10.1007/s11547-025-02074-z](https://doi.org/10.1007/s11547-025-02074-z).
- H. Yang, **S. Jung**, and J. T. Kwak. “From pathology to radiology: evaluating the applicability of pathology foundation models.” In *Foundation Models for General Medical AI (MedAGI 2025)*, Lecture Notes in Computer Science, vol. 16112, pp. 34–43, Springer, 2025. [doi:10.1007/978-3-032-07845-2_4](https://doi.org/10.1007/978-3-032-07845-2_4).
- H. J. Ki, H. G. Roh, J. T. Kwak, I. S. Kim, J. J. Park, Y. S. Jeon, H. Yang, **S. Jung**, J. S. Lee, and H. J. Kim. “The CT collateral map: collateral perfusion estimation and baseline lesion assessment after acute anterior circulation ischemic stroke.” *La Radiologia Medica*, 130(2):235–247, 2025. [doi:10.1007/s11547-024-01941-5](https://doi.org/10.1007/s11547-024-01941-5).
- Y. J. Jeon, H. G. Roh, **S. Jung**, H. Yang, H. J. Ki, J. J. Park, T.-J. Lee, N. I. Shin, J. S. Lee, J. T. Kwak, and H. J. Kim. “Clinical feasibility of deep learning-driven magnetic resonance angiography collateral map in acute anterior circulation ischemic stroke.” *Scientific Reports*, 15, Article 2304, 2025. [doi:10.1038/s41598-025-85731-7](https://doi.org/10.1038/s41598-025-85731-7).
- E. de la Rosa, R. Su, M. Reyes, et al. (including H. Yang, J. T. Kwak, and **S. Jung**). “ISLES'24: Final Infarct Prediction with Multimodal Imaging and Clinical Data. Where Do We Stand?” *arXiv:2408.10966*, 2024 (rev. 2025). [arxiv.org/abs/2408.10966](https://arxiv.org/abs/2408.10966). *Preprint.*
- **S. Jung**, H. Yang, H. J. Kim, H. G. Roh, and J. T. Kwak. “3D mobile regression vision transformer for collateral imaging in acute ischemic stroke.” *International Journal of Computer Assisted Radiology and Surgery*, 19(10):2043–2054, 2024. [doi:10.1007/s11548-024-03229-5](https://doi.org/10.1007/s11548-024-03229-5).
- H. Yang, **S. Jung**, V. T. L. Trinh, B. C. Doanh, J. Wang, H. G. Roh, H. J. Kim, and J. T. Kwak. “Investigation of Deep Learning Models and Training Strategies for Brain Stroke Segmentation.” *IEIE Annual Conference*, 2024.

Presentations & Challenges
======

- Hyun Yang, **Sumin Jung**, and Jin Tae Kwak. “From Pathology to Radiology: Evaluating the Applicability of Pathology Foundation Models.” Poster, MedAGI Workshop at MICCAI 2025, Sep. 2025.
- Hyun Yang, **Sumin Jung**, and Jin Tae Kwak. “3D Vision Transformer Based Infarct Segmentation.” ISLES 2024 Challenge, 2024.
- **Sumin Jung**. “3D Mobile Regression Vision Transformer for Collateral Imaging in Acute Ischemic Stroke.” Poster and three-minute oral presentation, CARS 2024, Jun. 2024.

Honors & Awards
======

- **Best Poster Award**, 38th Annual Conference of the Korean Society of Medical Imaging Informatics, 2024
- **9th Place**, Ischemic Stroke Lesion Segmentation Challenge (ISLES 2024), 2024
- **Honorable Mention**, Samsung AI Challenge, Image Quality Assessment, 2023
- **Gold Prize**, Joint Capstone Design Competition, 2022

Patent
======

Hyun Yang, **Sumin Jung**, and Hong Gee Roh. “Machine Learning Method for Generating Hypoperfusion Lesion Segmentation Maps from Cerebral Collateral Blood Flow Images Obtained Using Multi-Phase Dynamic Images, and a Method and System for Predicting Ischemic Penumbra Area Using Generated Hypoperfusion Lesion Segmentation Maps.” *Republic of Korea Patent Application No. 10-2024-0117934*, Aug. 2024. **Co-inventor.**

- Co-led development of the 3D medical-image framework for generating hypoperfusion lesion segmentation maps using anatomical information.

Teaching Experience
======

### Machine Learning and Intelligence for Electrical and Electronic Engineers

*Teaching Assistant, Korea University, Spring 2024*

- Ran lab sessions.
- Answered student questions and provided academic support.
