---
title: "Reducing MRI Acquisition Times with Deep Learning (ScattNet-MR)"
collection: talks
type: "Conference talk"
permalink: /talks/2025-mexcas-scattnetmr/
venue: "XXI Simposio Mexicano de Computación y Robótica en Medicina (MEXCAS 2025)"
date: 2025-09-04
location: "Auditorio Raúl J. Marsal, Faculty of Engineering, UNAM (Mexico City)"
---

[Download slides (PDF)](/files/talks/2025-supercomputo-scattnetmr.pdf)

### Overview

At **MEXCAS 2025**, I presented the same work delivered at the  
**Congreso Internacional de Supercómputo UNAM 2025**:  
a deep-learning framework called **ScattNet-MR**, designed to *significantly reduce MRI acquisition times while preserving diagnostic fidelity*.

This project integrates:

- **Super-resolution techniques**,  
- **Statistical physics**,  
- **Wavelet Scattering Transform (WST)**, and  
- A **residual convolutional architecture with attention**,  

to reconstruct high-quality MRI images from heavily undersampled k-space data.

The method achieves up to **75% reduction in scan time** without degrading critical anatomical information.

---

### Motivation

Modern MRI presents a critical bottleneck:

- Long acquisition times (~20 minutes per study)  
- High equipment cost  
- Limited access in Mexico (<3 scanners per million inhabitants)  

This results in delays for diagnosis and treatment.  
ScattNet-MR aims to address these systemic constraints by accelerating acquisition without sacrificing medical reliability.

---

### Method Summary

ScattNet-MR reconstructs high-quality MRI images by combining:

#### **Wavelet Scattering Transform (WST)**
A mathematically stable, multi-scale representation that:

- Captures non-Gaussian and structural information  
- Is robust to local deformations  
- Provides a physically interpretable loss function  

#### **Residual CNN with attention**
Learns the mapping from undersampled MRI slices to full-resolution images using:

- Multi-channel feature fusion  
- Statistical consistency enforced by WST-based KL divergence  
- Regularization against hallucinations common in GAN-based MRI models  

---

### Dataset & Training

The model was trained on the **fastMRI** dataset (Facebook AI Research + NYU Langone Health), using:

- 5000 MRI slices  
- Acceleration factors of **2×** and **4×**  
- 14 hours of training on an **NVIDIA RTX 4090**  
- 3.3M trainable parameters  

---

### Results

- High structural similarity (SSIM) for both 2× and 4× acceleration  
- Strong robustness to Gaussian acquisition noise  
- Superior stability compared to CNN-only baselines  
- Competitive performance with GAN models while using *far fewer parameters* and offering better interpretability  

ScattNet-MR enables complex statistical experiments (e.g., Monte-Carlo dropout) to run efficiently on consumer-grade GPUs.

---

### Clinical Potential

ScattNet-MR has direct impact on:

- Patient throughput  
- Workflow efficiency  
- Early disease detection  
- Computationally efficient MRI-based research  

Its physics-aware design reduces the risk of hallucinated structures, supporting safer medical deployment.

---

