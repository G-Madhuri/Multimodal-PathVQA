# PathVQA: Multimodal Visual Question Answering for Pathology Image Understanding

<p align="center">
  <img src="assets/banner.png" width="900">
</p>

## Overview

This repository contains the implementation, experiments, and analysis for our project:

> **PathVQA: Multimodal Visual Question Answering for Pathology Image Understanding**

The project focuses on developing deep learning-based Visual Question Answering (VQA) systems for pathology images using multiple multimodal architectures.

We extensively experimented with:
- CNN-based image encoders
- Vision Transformers
- Text Transformers
- Attention mechanisms
- Bilinear fusion methods
- Region-based visual reasoning

The project evaluates and compares multiple architectures on the **PathVQA dataset**.

---

# Project Objectives

- Build multimodal VQA systems for pathology image understanding
- Improve open-ended answer generation
- Compare CNNs vs Vision Transformers for medical imaging
- Study the effect of fusion strategies in multimodal learning
- Analyze attention-based reasoning for pathology VQA

---

# Dataset

## PathVQA Dataset

The dataset consists of pathology images paired with medical questions and answers.

| Property | Value |
|---|---|
| Total QA Pairs | 32,799 |
| Unique Images | 4,998 |
| Train Images | 2,499 |
| Validation Images | 1,499 |
| Test Images | 1,000 |

## Question Types
- What
- Yes/No
- Where
- How
- Others

## Original Paper
He et al., 2020  
https://arxiv.org/abs/2003.10286

---

# Implemented Methods

---

# Method 1 — Faster R-CNN + GRU + BAN

## Architecture
- Vision Encoder: Faster R-CNN
- Text Encoder: GRU
- Fusion: Bilinear Attention Network (BAN)

## Key Features
- Region-based visual reasoning
- Attention-driven fusion
- Fine-grained image-text interaction

## Performance

| Metric | Score |
|---|---|
| Overall EM | 46.03% |
| Yes/No Accuracy | 78.03% |
| Open-ended EM | 34.26% |
| F1 Score | 34.77% |

---

# Method 2 — EfficientNet-B0 + BiLSTM + Bilinear Fusion

## Architecture
- Vision Encoder: EfficientNet-B0
- Text Encoder: BiLSTM
- Fusion: Bilinear Fusion

## Key Features
- Best overall performing model
- Strong multimodal feature interaction
- Extensive CNN and fusion experimentation

## Performance

| Metric | Score |
|---|---|
| Overall EM | 59.09% |
| Yes/No Accuracy | 82.28% |
| Open-ended EM | 50.56% |
| F1 Score | 50.92% |

---

# Method 3 — ResNet50 + Stacked Attention + LayerNorm

## Architecture
- Vision Encoder: ResNet50
- Text Encoder: LSTM
- Attention: Stacked Attention Network
- Normalization: LayerNorm

## Key Features
- Iterative visual reasoning
- Attention-based pathology understanding
- Strong open-ended answer performance

## Performance

| Metric | Score |
|---|---|
| Overall EM | 56.24% |
| Yes/No Accuracy | 82.27% |
| Open-ended EM | 46.66% |
| F1 Score | 47.82% |

---

# Experimental Findings

## Key Insights

- Bilinear fusion significantly improves multimodal learning
- CNNs outperform Vision Transformers on pathology images
- Fusion strategy matters more than backbone complexity
- Attention mechanisms improve reasoning capability
- Region-based models help localization tasks

---

# Repository Structure

```bash
PathVQA/
│
├── Method1_FasterRCNN_GRU_BAN/
│   ├── notebooks/
│   ├── models/
│   ├── outputs/
│   └── README.md
│
├── Method2_EfficientNet_BiLSTM/
│   ├── notebooks/
│   ├── models/
│   ├── outputs/
│   └── README.md
│
├── Method3_ResNet_Attention/
│   ├── notebooks/
│   ├── models/
│   ├── outputs/
│   └── README.md
│
├── assets/
├── presentation/
├── requirements.txt
└── README.md
```

---

# Technologies Used

## Deep Learning
- PyTorch
- Torchvision
- Transformers

## Models
- EfficientNet
- ResNet50
- Faster R-CNN
- BiLSTM
- GRU
- BAN
- Stacked Attention Networks

## Tools
- Kaggle


---

# Installation

## Clone Repository

```bash
git clone https://github.com/yourusername/PathVQA.git
cd PathVQA
```

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

# Running the Project

## Method 1

```bash
cd Method1_FasterRCNN_GRU_BAN
```

Run notebooks in order.

---

## Method 2

```bash
cd Method2_EfficientNet_BiLSTM
```

Run notebooks in order.

---

## Method 3

```bash
cd Method3_ResNet_Attention
```

Run notebooks in order.

---

# Results Summary

| Method | Best Architecture | Overall EM |
|---|---|---|
| Method 1 | Faster R-CNN + BAN | 46.03% |
| Method 2 | EfficientNet-B0 + Bilinear | 59.09% |
| Method 3 | ResNet50 + Attention | 56.24% |

---

# Future Work

- Multimodal Compact Bilinear Pooling (MCB)
- Retrieval-Augmented Generation (RAG)
- Contrastive multimodal learning
- Large Vision-Language Models
- Clinical deployment validation
- Explainable medical VQA

---

# References

1. He et al. — PathVQA (2020)  
2. BaMCo (2025)  
3. Path-RAG (2024)  
4. BLIP (2022)  
5. EfficientNet (2019)  
6. Multimodal Compact Bilinear Pooling (2016)

---

# Authors

- Madhuri Gottumukkala
- Srivarsha Chivukula
- Peesari Sathvik Reddy

Department of Artificial Intelligence & Machine Learning  
Chaitanya Bharathi Institute of Technology

---

# License

This project is for academic and research purposes.
