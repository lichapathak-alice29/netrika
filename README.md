
# 👁️ NETRIKA

### Explainable AI for Diabetic Retinopathy Screening in Rural India

> **See the signs. Understand the AI. Support the decision.**

---

<p align="center">
  <img src="https://img.shields.io/badge/SIH%202026-Problem%20Statement%2026038-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/AI-Explainable%20AI-purple?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Domain-MedTech%20%7C%20HealthTech-red?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Platform-Web%20%7C%20AI-green?style=for-the-badge" />
</p>

---

## 🌿 What is NETRIKA?

**NETRIKA** is an AI-assisted retinal screening platform designed to support the early screening and severity assessment of **Diabetic Retinopathy (DR)** from fundus images.

NETRIKA analyses a retinal image, predicts the **DR severity level from 0–4**, identifies potentially **referable cases**, and explains the model's prediction using **Grad-CAM visualizations**.

The system is designed as a **decision-support tool**, keeping an ophthalmologist in the loop for the final clinical assessment.

> **NETRIKA does not replace an ophthalmologist. It helps them see, understand, and prioritize.**

---

## 🎯 The Problem

Diabetic Retinopathy can cause preventable vision loss when it is not detected and managed early.

In rural India, large-scale manual screening is difficult because specialist resources are limited. Retinal images captured in field conditions can also vary significantly in quality.

The challenge is therefore not only:

> **“Can AI detect DR?”**

but also:

> **“Can AI provide a reliable, explainable screening result that a healthcare professional can review?”**

NETRIKA addresses this through an integrated screening workflow.

---

# 💡 Our Solution

NETRIKA combines **AI-based DR classification, image-quality assessment, explainability, and human review** into one workflow.

```text
                    👤 PATIENT
                        │
                        ▼
              📷 FUNDUS IMAGE
                        │
                        ▼
             🔍 IMAGE QUALITY CHECK
                        │
                ┌───────┴───────┐
                │               │
              POOR            GOOD
                │               │
                ▼               ▼
          🔄 RECAPTURE      🧹 PREPROCESSING
                                │
                                ▼
                         🧠 AI SCREENING
                                │
                                ▼
                       DR SEVERITY 0–4
                                │
                       ┌────────┴────────┐
                       │                 │
                       ▼                 ▼
                  📊 RESULT         🔥 GRAD-CAM
                       │                 │
                       └────────┬────────┘
                                ▼
                       👨‍⚕️ DOCTOR REVIEW
                                │
                                ▼
                         📄 FINAL REPORT
````

---

# ⭐ Core Features

## 🧠 01 — Explainable AI Screening

NETRIKA analyses fundus images and predicts the severity of Diabetic Retinopathy.

| Level | Severity         |
| :---: | ---------------- |
| **0** | No DR            |
| **1** | Mild DR          |
| **2** | Moderate DR      |
| **3** | Severe DR        |
| **4** | Proliferative DR |

### Referable DR

Cases at:

**Level 2+**

are identified as potentially **referable** for specialist review.

---

# 🔥 02 — Grad-CAM Explainability

A prediction without an explanation can be difficult for a clinician to interpret.

NETRIKA therefore provides a **Grad-CAM attention map** showing the retinal regions that contributed to the model's prediction.

```text
┌──────────────────┐
│  RETINAL IMAGE   │
└────────┬─────────┘
         │
         ▼
   🧠 AI MODEL
         │
         ▼
   ┌─────────────┐
   │  Grad-CAM   │
   │  Heatmap    │
   └─────────────┘
         │
         ▼
  🔎 VISUAL EVIDENCE
```

The ophthalmologist can view:

* Original retinal image
* Grad-CAM heatmap
* Heatmap overlay
* AI prediction
* Model probability/confidence

This makes the model's decision more transparent.

---

# 🔍 03 — Image Quality Assessment

Poor-quality images should not blindly enter the classification pipeline.

NETRIKA checks:

* **Focus / Blur**
* **Illumination**
* **Field of View**

### Example

```text
IMAGE QUALITY
━━━━━━━━━━━━━━━━━━━━

Focus          ✓ Good
Illumination   ✓ Good
Field of View  ✓ Good

STATUS
🟢 GRADABLE
```

If the image is unsuitable:

```text
IMAGE QUALITY
━━━━━━━━━━━━━━━━━━━━

Focus          ✗ Poor
Illumination   ✓ Good
Field of View  ✓ Good

STATUS
🔴 NOT GRADABLE

Please recapture the retinal image.
```

This creates a quality gate before AI screening.

---

# 👨‍⚕️ 04 — Human-in-the-Loop Review

NETRIKA is **not an autonomous diagnostic system**.

The AI provides screening assistance.

The ophthalmologist makes the final clinical assessment.

### AI provides

* DR severity prediction
* Model probability/confidence
* Grad-CAM visualization
* Screening evidence

### Ophthalmologist provides

* Clinical review
* Final assessment
* Referral decision

```text
       AI SCREENING
             │
             ▼
       AI EXPLANATION
             │
             ▼
     👨‍⚕️ OPHTHALMOLOGIST
             │
             ▼
      FINAL ASSESSMENT
```

---

# 📄 05 — Screening Report

After screening and review, NETRIKA can generate a structured report containing:

```text
Patient ID
──────────────
P1024

Image Quality
──────────────
Gradable

DR Severity
──────────────
Level 2 — Moderate DR

Referable
──────────────
YES

Model Probability
──────────────
[Model Output]

Explainability
──────────────
Grad-CAM Included

Doctor Review
──────────────
[Final Assessment]
```

---

# 📍 06 — Referral Support

For potentially referable cases, NETRIKA can provide a pathway toward specialist care.

The future version can support:

* Nearby ophthalmologists
* Healthcare facilities
* Distance
* Contact information

This feature remains **secondary to the core AI screening system**.

---

# 🧬 AI Pipeline

```text
Fundus Image
     │
     ▼
Image Quality Assessment
     │
     ▼
Image Preprocessing
     │
     ├── Resize
     ├── Normalization
     ├── CLAHE
     └── Denoising
     │
     ▼
Deep Learning Model
     │
     ▼
DR Classification
     │
     ├── Level 0
     ├── Level 1
     ├── Level 2
     ├── Level 3
     └── Level 4
     │
     ▼
Referable DR Detection
     │
     ▼
Grad-CAM
     │
     ▼
Explainable Screening Result
```

---

# 🏗️ System Architecture

```text
┌──────────────────────────────────────────┐
│              NETRIKA UI                  │
│                                          │
│  Healthcare Worker │ Ophthalmologist     │
└───────────────────┬──────────────────────┘
                    │
                    ▼
┌──────────────────────────────────────────┐
│              BACKEND / API               │
│                                          │
│       Patient & Screening Management     │
└───────────────────┬──────────────────────┘
                    │
                    ▼
┌──────────────────────────────────────────┐
│          AI / IMAGE PIPELINE             │
│                                          │
│ Quality → Preprocessing → DR Model       │
│                         → Grad-CAM       │
└───────────────────┬──────────────────────┘
                    │
                    ▼
┌──────────────────────────────────────────┐
│               DATABASE                   │
│                                          │
│ Patients │ Results │ Reviews │ Reports   │
└──────────────────────────────────────────┘
```

---

# 🌐 Rural Screening Workflow

NETRIKA is designed around a rural healthcare scenario:

```text
🏠 Patient
    │
    ▼
🏥 Rural Screening Centre
    │
    ▼
👩‍⚕️ Healthcare Worker
    │
    ▼
📷 Fundus Image
    │
    ▼
👁️ NETRIKA
    │
    ├── Image Not Gradable
    │        ↓
    │    Recapture
    │
    └── Gradable
           ↓
      AI Screening
           ↓
     Explainable Result
           ↓
    Potentially Referable
           ↓
    👨‍⚕️ Ophthalmologist
           ↓
      Final Assessment
```

---

# 📊 Large-Scale Deployment Simulation

The problem statement also requires a **Simulink-based simulation** of the screening workflow.

NETRIKA can model:

* Patient arrival rate
* Image acquisition rate
* Data transmission
* Bandwidth constraints
* AI processing throughput
* Ophthalmologist review capacity
* Screening workload

### Example

```text
100,000+ Patients / Year
          │
          ▼
   Image Acquisition
          │
          ▼
      AI Screening
          │
          ▼
   Referable Cases
          │
          ▼
Ophthalmologist Capacity
          │
          ▼
   Review Workload
```

The objective is to understand how the screening pipeline could operate at district scale.

---

# 🧪 Datasets

The SIH problem statement provides the following datasets as potential resources:

### APTOS 2019

DR severity classification.

### IDRiD

Indian retinal images with DR-related annotations.

### DRIVE

Retinal vessel extraction.

### Messidor-2

Retinal image dataset for DR research.

Different datasets may be used for different components of the pipeline rather than forcing the entire system onto a single dataset.

---

# 🛠️ Technology Stack

### AI & Image Processing

* MATLAB
* Image Processing Toolbox
* Computer Vision Toolbox
* Deep Learning Toolbox
* Medical Imaging Toolbox
* Statistics and Machine Learning Toolbox
* Grad-CAM

### Simulation

* Simulink

### Frontend

* React
* JavaScript
* HTML
* CSS

### Backend

* Python
* FastAPI
* REST API

### Database

* MongoDB / PostgreSQL

---

# 📈 Model Evaluation

NETRIKA will evaluate the AI model using metrics such as:

* Accuracy
* Sensitivity
* Specificity
* Precision
* F1-score
* Confusion Matrix
* ROC-AUC

The SIH problem statement specifies a target of:

> **Sensitivity > 90% and Specificity > 85% for referable DR.**

These are **target evaluation criteria**, not claims about model performance unless demonstrated through appropriate testing.

---

# 🔐 Responsible AI

NETRIKA follows a **human-in-the-loop** approach.

### We do NOT claim:

❌ Autonomous diagnosis
❌ Replacement of ophthalmologists
❌ 100% accurate predictions
❌ AI certainty

### We provide:

✅ AI-assisted screening
✅ Explainable predictions
✅ Image-quality rejection
✅ Referral prioritization
✅ Specialist review
✅ Transparent model limitations

---

# 🎯 Project Objectives

* Develop an AI-based DR screening pipeline.
* Classify retinal images into DR Levels 0–4.
* Identify potentially referable cases.
* Reject ungradable retinal images.
* Explain predictions using Grad-CAM.
* Support ophthalmologist-led review.
* Generate structured screening reports.
* Simulate large-scale rural deployment using Simulink.

---

# 💎 What Makes NETRIKA Different?

Most importantly, NETRIKA is **not just a DR classifier**.

Our focus is:

```text
             DETECT
                +
             EXPLAIN
                +
             VERIFY
                +
             REFER
```

### **AI that doesn't just give an answer — it shows where the answer came from.**

---

# 🚀 Development Roadmap

### Phase 1 — AI Foundation

```text
Dataset
   ↓
Preprocessing
   ↓
DR Classification
   ↓
Level 0–4
   ↓
Model Evaluation
```

### Phase 2 — Explainability

```text
DR Model
   ↓
Grad-CAM
   ↓
Visual Explanation
```

### Phase 3 — Reliability

```text
Image Quality
   ↓
Gradable / Not Gradable
   ↓
AI Screening
```

### Phase 4 — Product

```text
Frontend
   +
Backend
   +
AI Pipeline
   ↓
Doctor Review
   ↓
Screening Report
```

### Phase 5 — Scale

```text
Simulink
   ↓
Rural Telemedicine Simulation
   ↓
Resource Optimization
```

---

# 🧭 Project Scope

### 🔴 Core

* DR Level 0–4 classification
* Referable DR detection
* Grad-CAM explainability
* Image quality assessment

### 🟡 Supporting

* Ophthalmologist review
* Screening report

### 🟢 Optional

* Nearby ophthalmologist discovery
* Additional advanced lesion analysis

We deliberately avoid unrelated features such as fitness tracking, diet planning, ambulance tracking, chatbots, and appointment management.

**The goal is depth, not feature count.**

---

# ⚠️ Disclaimer

NETRIKA is an academic/research prototype developed for **AI-assisted screening and decision support**.

It is not intended to replace professional ophthalmological examination or provide an independent clinical diagnosis.

Final clinical decisions must be made by qualified healthcare professionals.

---

# 👥 Team

**Project:** NETRIKA

**SIH 2026 Problem Statement:** 26038

**Organization:** MathWorks

**Theme:** MedTech / BioTech / HealthTech

---

## 👁️ NETRIKA

### *Explain. Screen. Refer.*

**AI-assisted retinal screening for a more accessible future of eye care.**


