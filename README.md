# RetinaXplain 🩺👁️

### Explainable AI for Diabetic Retinopathy Screening in Rural India

RetinaXplain is an AI-assisted retinal screening platform designed to support the early detection and severity assessment of **Diabetic Retinopathy (DR)** from fundus images.

The system analyses retinal images, predicts the DR severity level from **0–4**, identifies potentially referable cases, and uses **Explainable AI (Grad-CAM)** to show the retinal regions that influenced the model's prediction.

> **AI assists the screening process. It does not replace an ophthalmologist or provide a final clinical diagnosis.**

---

## 🎯 Problem

Diabetic Retinopathy is a major complication of diabetes that can lead to preventable vision loss.

In rural areas, access to ophthalmologists can be limited, making large-scale manual retinal screening difficult.

Poor-quality retinal images can also lead to unreliable AI predictions.

RetinaXplain aims to provide an AI-assisted screening workflow that can help identify potentially serious cases and prioritize them for specialist review.

---

## 💡 Our Solution

The platform follows this workflow:

```text
Patient
   ↓
Retinal / Fundus Image
   ↓
Image Quality Assessment
   ↓
Image Preprocessing
   ↓
AI-based DR Classification
   ↓
DR Severity Level 0–4
   ↓
Referable DR Detection
   ↓
Grad-CAM Explainability
   ↓
Ophthalmologist Review
   ↓
Screening Report
