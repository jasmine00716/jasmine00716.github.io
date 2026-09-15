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

### 3D-MoReT: Collateral Imaging from 4D MR Perfusion

*First Author and Lead Researcher, Korea University, 2023–2024 · [Project and code](https://github.com/jasmine00716/3D-MoReT)*

- Led the study from problem formulation and data preprocessing through model design, implementation, experiments, comparative analysis, and initial manuscript drafting.
- Designed a 3D CNN–Transformer regression model combining MobileNetV2, MobileViT, ViT, and residual/skip connections to generate five-phase collateral maps from 4D DSC-MRP.
- Evaluated the model on 952 patients from two university hospitals; outperformed similarly sized models and matched substantially heavier baselines.
- Published the work as first author in the *International Journal of Computer Assisted Radiology and Surgery* and presented it at CARS 2024.

### PathRadX: Pathology Foundation Models for Radiology

*Contributing Researcher, Korea University, 2025*

- Supported data preparation, result analysis, and manuscript drafting for a study evaluating whether a frozen pathology foundation model could transfer to radiology tasks.
- Contributed to experiments spanning MURA, RSNA pneumonia, and MedFMC datasets and comparisons of modality-adaptation and task-classification strategies; collaborators led model design, implementation, and experiment execution.
- Published in the MedAGI 2025 workshop proceedings held with MICCAI 2025.

### ISLES 2024: Multimodal Infarct Segmentation

*Research Design and Analysis, Korea University, 2024*

- Contributed problem definition, data preparation, method and experimental design, comparative analysis, and abstract preparation for a 3D Vision Transformer using NCCT, CTP, CTA, and Tmax inputs.
- Collaborated with a teammate who implemented the code and ran the experiments.
- The team placed ninth in the ISLES 2024 Challenge; Sumin Jung was subsequently included as a co-author of the challenge's revised 2025 arXiv preprint.

Industry Experience
======

### DeepClue Inc., Seoul, Republic of Korea

*Team Leader, Engineering & Manufacturing Team, Sep. 2024 – Jun. 2026*

- Led the translation of collateral-imaging research into DeepClue-Precise MRI/CT software as a medical device (SaMD), coordinating clinical requirements, system architecture, implementation, verification, regulatory documentation, and team operations.
- Developed the MRI application and image-processing pipeline end to end, including DICOM preprocessing, image analysis, GUI, output generation, and testing.
- Designed the reusable application framework adopted by the CT product and collaborated with the developer responsible for its CT-specific core image-processing pipeline.
- Designed and executed software verification and validation, prepared regulatory and quality-system documents, coordinated with hospitals and external organizations, and led activities supporting MFDS Class I medical-device registration.
- Supported hospital prototype deployment and converted clinical feedback into software requirements and validation criteria.

Journal Articles
======

<ul>
{% assign journal_publications = site.publications | where: "category", "manuscripts" | reverse %}
{% for post in journal_publications %}
  {% include archive-single-cv.html %}
{% endfor %}
</ul>

Conference Papers & Preprints
======

<ul>
{% assign conference_publications = site.publications | where: "category", "conferences" | reverse %}
{% for post in conference_publications %}
  {% include archive-single-cv.html %}
{% endfor %}
</ul>

Presentations & Challenges
======

- **Sumin Jung**. “3D Mobile Regression Vision Transformer for Collateral Imaging in Acute Ischemic Stroke.” Poster and three-minute oral presentation, CARS 2024, Jun. 2024.
- Hyun Yang, **Sumin Jung**, and Jin Tae Kwak. “From Pathology to Radiology: Evaluating the Applicability of Pathology Foundation Models.” Poster, MedAGI Workshop at MICCAI 2025, Sep. 2025.
- Hyun Yang, **Sumin Jung**, and Jin Tae Kwak. “3D Vision Transformer Based Infarct Segmentation.” ISLES 2024 Challenge, 2024.
- Hee Jong Ki, Hong Gee Roh, Sang Bong Lee, Jin Tae Kwak, Jeong Jin Park, Hyung Jin Lee, Yoo Sung Jeon, **Sumin Jung**, Hyun Yang, Cheolhee Yu, Ji Sung Lee, and Hyun Jeong Kim. “Collateral Perfusion Score as a Surrogate of Infarct Growth Rate and Predictor of Futile Endovascular Thrombectomy in Acute Anterior Circulation Ischemic Stroke.” Poster, ICSU & ICAS 2025, Nov. 2025. [Abstract book](https://www.strokeupdate-kss.org/file/ICSU%26ICAS%202025_Abstract%20Book.pdf)

Honors & Awards
======

- **Best Poster Award**, 38th Annual Conference of the Korean Society of Medical Imaging Informatics, 2024
- **9th Place**, Ischemic Stroke Lesion Segmentation Challenge (ISLES 2024), 2024
- **Honorable Mention**, Samsung AI Challenge, Image Quality Assessment, 2023
- **Gold Prize**, Joint Capstone Design Competition, 2022

Patent Application
======

Hyun Yang, **Sumin Jung**, and Hong Gee Roh. “Machine Learning Method for Generating Hypoperfusion Lesion Segmentation Maps from Cerebral Collateral Blood Flow Images Obtained Using Multi-Phase Dynamic Images, and a Method and System for Predicting Ischemic Penumbra Area Using Generated Hypoperfusion Lesion Segmentation Maps.” *Republic of Korea Patent Application No. 10-2024-0117934*, Aug. 2024. **Co-inventor.**

- Co-developed a 3D medical-image framework for generating hypoperfusion lesion segmentation maps using anatomical information.

Technical Skills
======

- **Programming:** Python; C; Java; JavaScript; SQL
- **Machine Learning:** PyTorch; TensorFlow; scikit-learn; 3D CNNs; U-Net; Transformers; regression; segmentation; classification
- **Medical Imaging:** DICOM; pydicom; MR/CT preprocessing; multi-vendor clinical imaging pipelines
- **Scientific Computing:** NumPy; pandas; OpenCV; scikit-image; matplotlib; R
- **Development Tools:** Git; Docker; Jupyter; PyCharm; Visual Studio Code; PySimpleGUI; PyQt6
