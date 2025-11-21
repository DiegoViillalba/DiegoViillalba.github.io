---
title: "Super-Resolution in Cosmological Simulations"
collection: talks
type: "Conference talk"
permalink: /talks/2025-rea-superresolution/
venue: "Reunión de Estudiantes de Astronomía (REA), UNAM 2025"
date: 2025-06-25
location: "Instituto de Astronomía, UNAM (Mexico City)"
---

[Download slides (PDF)](/files/talks/2025-rea-superresolution.pdf)

### Overview

This talk, presented at the **Reunión de Estudiantes de Astronomía (REA) 2025**, introduces a super-resolution framework for cosmological simulations that combines **deep generative models** with the **Wavelet Scattering Transform (WST)** to enhance the resolution of dark-matter density fields.

The work addresses a key challenge in modern computational cosmology:  
> **High-resolution N-body simulations are extremely expensive, while low-resolution runs lose crucial small-scale information.**  


By integrating WST into a residual generative architecture, the method recovers small-scale structure while preserving the statistical and physical properties of the underlying cosmological field.

---

### Motivation

Cosmological simulations face an inherent trade-off:

- **High resolution → extremely expensive CPU/GPU time + large storage**  
- **Low resolution → loss of small-scale halos, filaments, and non-Gaussian structure**

Existing deep-learning super-resolution approaches (GANs, VAEs, diffusion models) suffer from:

- Instability during training  
- Hallucination of non-physical structures  
- Loss of cosmological statistics  
- Poor interpretability  
*(Slides 1–3)*  

---

### Approach: Wavelet-Based Generative Super-Resolution

The method incorporates the **Wavelet Scattering Transform** (WST) into a deep residual architecture to stabilize training and preserve physical information.

#### Why WST?

- Captures multi-scale structure  
- Stable to deformations and small translations  
- Sensitive to non-Gaussian statistics  
- Avoids phase reconstruction issues typical of Fourier-based approaches  
*(Slides 16–21)*  

WST coefficients serve as a **statistical loss function** that forces the network to match the high-resolution distribution of cosmological fields.

---

### Dataset: Illustris Simulations

Training is performed using slices from the **Illustris** family of simulations:

- **Illustris-3** → low-resolution input  
- **Illustris-2** → high-resolution target  

Each slice:  
- Thickness: **0.25 Mpc**  
- Paired dataset: **7200 LR/HR image pairs**  
*(Slides 23–26)*  

Split into:  
- 90% training  
- 10% validation  
- 800 images for testing

---

### Network Architecture

The proposed architecture includes:

- Two feature extraction branches (LR features + WST features)  
- Feature fusion layer  
- **n** residual Squeeze-and-Excitation (SE) blocks  
- Output reconstruction layer  
*(Slides 27–28)*  

Loss functions explored:

- L2 (MSE)  
- Perceptual loss  
- **WST-based loss** (best performance)  
*(Slides 29–32)*  

Training:

- Performed on an **RTX 4090 (24 GB VRAM)**  
- ~8 hours per training run  
*(Slide 32)*

---

### Results

#### Qualitative Reconstruction  
The model reconstructs higher-resolution structures that closely resemble **Illustris-2**, while avoiding hallucinations typical of GAN-based methods.  
*(Slides 33–36)*  

#### Power Spectrum Evaluation  
A physically meaningful test is performed by comparing the recovered **power spectrum P(k)**:

- Bicubic interpolation → severe loss of small-scale power  
- L1/Perceptual loss → improved but imperfect  
- **WST loss → closest match to ground truth across a wide k-range**, even up to k ≈ 5–6 h/Mpc  
*(Slide 36)*  

#### Peak and Valley Counts  
The model also preserves higher-order morphological statistics like:

- Density of local maxima  
- Density of local minima  
*(Slides 37–39)*  

---

### Conclusions

- WST-based super-resolution produces **physically consistent reconstructions** of cosmological fields.  
- Recovers statistical properties (P(k), peaks/valleys) better than standard approaches.  
- Provides a more interpretable alternative to GANs and VAEs.  
- Has potential to **augment low-resolution simulations** and reduce computational demands for large parameter scans.  
*(Slides 40–41)*  

---

### Future Work

- Increase network capacity with more residual blocks  
- Incorporate additional WST scales  
- Extend to fully 3D super-resolution  
- Train on larger, multi-institutional cosmology datasets  
*(Slide 41)*  

---


