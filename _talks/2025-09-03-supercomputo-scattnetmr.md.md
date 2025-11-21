---
title: "Reducing MRI Acquisition Times: A Deep Learning Solution (ScattNet-MR)"
collection: talks
type: "Conference talk"
permalink: /talks/2025-supercomputo-scattnetmr/
venue: "Congreso Internacional de Supercómputo UNAM 2025"
date: 2025-09-03
location: "Auditorio Sotero Prieto, Faculty of Engineering, UNAM (Mexico City)"
---
### **Slides**

- [Download slides (PDF)](/files/talks/2025-supercomputo-scattnetmr.pdf)

### **Overview**

This talk was presented at the **Congreso Internacional de Supercómputo UNAM 2025**, where I introduced **ScattNet-MR**, a deep-learning-based framework designed to **reduce MRI acquisition times by up to 75%** while preserving diagnostic integrity.

The method integrates **super-resolution**, **statistical physics**, and the **Wavelet Scattering Transform (WST)** to create a robust, interpretable, and computationally efficient reconstruction model.  

---

### **Motivation**

Magnetic Resonance Imaging (MRI) is one of the most powerful non-invasive diagnostic tools, yet it suffers from:

- **Long scan times** (≈20 minutes per study)  
- **High operational costs**  
- **Very low scanner availability in Mexico** (<3 scanners per million inhabitants)  

This leads to long waiting times and delayed diagnoses, especially in resource-limited healthcare systems.  
*(Slides 1–3)* 

Reducing acquisition time is therefore critical for **patient throughput**, **clinical efficiency**, and **timely diagnosis**.

---

### **MRI Acquisition and the Bottleneck**

The talk includes an accessible overview of:

- Proton precession and Larmor frequency  
- k-space encoding via gradient fields  
- Image formation through the inverse Fourier Transform  
*(Slides 6–8)*  

The key limitation:  
> **Fully sampling k-space requires many repeated measurements**, creating the inherent time bottleneck.

---

### **Acceleration via Subsampling (and Its Problems)**

Reducing the number of phase-encoding lines leads to:

- Aliasing  
- Violations of the Nyquist sampling theorem  
- Severe reconstruction artifacts  
*(Slide 10)*

---

### **Deep Learning for Reconstruction**

Classical interpolation fails to recover lost high-frequency structure. Deep learning offers a nonlinear approach, but…  
*(Slides 11–17)*  

**Challenges of deep models in clinical reconstruction:**

- Risk of *hallucinations* (anatomically realistic but false details)  
- Global metrics (SSIM, PSNR) cannot guarantee structural correctness  
- Need for uncertainty estimation  
- Task-based evaluation by radiologists is essential  

---

### **Our Approach: ScattNet-MR**

ScattNet-MR is a **residual CNN with attention mechanisms**, trained not only on pixel-wise error but also using **statistical constraints derived from the Wavelet Scattering Transform**.  
*(Slides 18–24)*  

Key features:

- WST provides **stable, multiscale, and interpretable feature descriptors**  
- KL divergence between WST coefficient distributions penalizes unrealistic reconstructions  
- No need to reconstruct phases explicitly  
- Increased robustness and reduced hallucinations  

---

### **Dataset and Experimental Setup**

Using the **fastMRI** dataset, we simulated realistic subsampling at:

- **50% acquisition** (8% center lines)  
- **25% acquisition** (4% center lines)  
*(Slides 19–20)*  

Training details:

- 5000 MRI slices  
- **14 hours** on an NVIDIA RTX 4090  
- **3.3 million** trainable parameters  
*(Slide 25)*  

---

### **Results**

#### **Acceleration ×2**
ScattNet-MR achieves:

- High structural preservation  
- Improved SSIM vs. classical interpolation  
*(Slides 27–29)*  

#### **Acceleration ×4**
More challenging regime, yet the model still reconstructs realistic anatomical detail.  
*(Slides 30–32)*  

#### **Noise robustness**
When adding Gaussian noise, ScattNet-MR preserves structural consistency significantly better than CNN baselines.  
*(Slides 33–41)*  

#### **Comparisons**
- Outperforms simple CNN models  
- Slightly below GAN models in SSIM, but with *far fewer parameters* and *higher interpretability*  
*(Slides 42–43)*  

---

### **Conclusions**

- **Clinical relevance:** Reducing MRI acquisition time directly improves patient care and hospital throughput.  
- **Methodological innovation:** Wavelet-based statistical constraints mitigate hallucinations and enhance stability.  
- **Computational efficiency:** Enables Monte Carlo uncertainty quantification in practical time.  
*(Slide 45)*  

---

### **Future Work**
Potential improvements include:

- Designing lighter architectures without sacrificing accuracy  
- Extending the method to multi-coil and multi-institutional datasets  
- Adapting the model for CT or ultrasound reconstruction  
*(Slide 46)*  

---



