---
permalink: /
title: ""
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<style>
.about-wrapper {
  max-width: 720px;
}

.about-intro {
  margin-bottom: 2.5rem;
}

.about-intro .name-line {
  font-size: 1.75rem;
  font-weight: 700;
  letter-spacing: -0.03em;
  color: #1a1a1a;
  margin: 0 0 0.1rem;
  line-height: 1.2;
}

.about-intro .name-line span {
  color: #1a6fc4;
}

.about-intro .role-line {
  font-size: 0.85rem;
  font-weight: 600;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: #999;
  margin: 0 0 1.6rem;
}

.about-intro p {
  font-size: 0.97rem;
  line-height: 1.85;
  color: #333;
  margin-bottom: 1rem;
}

.about-intro a {
  color: #1a6fc4;
  text-decoration: none;
  border-bottom: 1px solid #c5d8f0;
  transition: border-color 0.15s;
}

.about-intro a:hover {
  border-color: #1a6fc4;
}

.focus-cards {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 0.75rem;
  margin: 1.8rem 0 2.2rem;
}

.focus-card {
  border: 1px solid #eaeaea;
  border-radius: 6px;
  padding: 0.9rem 1.1rem;
  background: #fafafa;
}

.focus-card-label {
  font-size: 0.7rem;
  font-weight: 700;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: #1a6fc4;
  margin-bottom: 0.3rem;
}

.focus-card-text {
  font-size: 0.87rem;
  color: #444;
  line-height: 1.5;
  margin: 0;
}

.section-rule {
  font-size: 0.7rem;
  font-weight: 700;
  letter-spacing: 0.13em;
  text-transform: uppercase;
  color: #bbb;
  border-bottom: 1px solid #ebebeb;
  padding-bottom: 0.4rem;
  margin: 2.2rem 0 1.2rem;
}

.interests-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 0.35rem 2rem;
  margin-bottom: 0.5rem;
}

.interest-item {
  font-size: 0.88rem;
  color: #333;
  padding: 0.3rem 0;
  border-bottom: 1px solid #f2f2f2;
  display: flex;
  align-items: baseline;
  gap: 0.5rem;
  line-height: 1.45;
}

.interest-item::before {
  content: '';
  display: inline-block;
  width: 4px;
  height: 4px;
  border-radius: 50%;
  background: #1a6fc4;
  flex-shrink: 0;
  margin-bottom: 1px;
}

.applications-row {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 0.75rem;
  margin: 1rem 0 0;
}

.app-card {
  border-left: 3px solid #1a6fc4;
  padding: 0.6rem 0.9rem;
  background: #f7faff;
  border-radius: 0 4px 4px 0;
}

.app-card-title {
  font-size: 0.8rem;
  font-weight: 700;
  letter-spacing: 0.04em;
  color: #1a6fc4;
  text-transform: uppercase;
  margin-bottom: 0.2rem;
}

.app-card-text {
  font-size: 0.85rem;
  color: #444;
  margin: 0;
  line-height: 1.5;
}

.personal-block {
  background: #fafafa;
  border: 1px solid #eaeaea;
  border-radius: 6px;
  padding: 1.1rem 1.3rem;
  margin-bottom: 2rem;
}

.personal-block p {
  font-size: 0.9rem;
  color: #444;
  line-height: 1.8;
  margin: 0 0 0.6rem;
}

.personal-block p:last-child {
  margin: 0;
}

.personal-block strong {
  color: #1a1a1a;
  font-weight: 600;
}

.photo-block {
  margin: 2rem 0;
}

.photo-block img {
  width: 100%;
  max-width: 580px;
  border-radius: 6px;
  border: 1px solid #eaeaea;
  display: block;
}

.cta-line {
  font-size: 0.9rem;
  color: #555;
  line-height: 1.7;
  margin-top: 1.5rem;
  padding-top: 1.5rem;
  border-top: 1px solid #ebebeb;
}

.cta-line a {
  color: #1a6fc4;
  text-decoration: none;
  font-weight: 500;
  border-bottom: 1px solid #c5d8f0;
}

.cta-line a:hover {
  border-color: #1a6fc4;
}

@media (max-width: 600px) {
  .focus-cards,
  .interests-grid,
  .applications-row {
    grid-template-columns: 1fr;
  }
  .about-intro .name-line {
    font-size: 1.4rem;
  }
}
</style>

<div class="about-wrapper">

<div class="about-intro">
  <p class="name-line">Diego <span>Villalba</span></p>
  <p class="role-line">Physics · Machine Learning · Scientific Computing</p>

  <p>
    I am a physicist working at the intersection of machine learning and scientific computing. My research focuses on cosmology, computational astrophysics, and the data-driven modeling of physical systems — with the goal of developing AI methods that are scalable, interpretable, and physically grounded.
  </p>

  <p>
    I am particularly drawn to the idea that machine learning and physics are not separate disciplines, but complementary frameworks that can be unified to address complex scientific, technological, and societal challenges. This perspective guides both my research and teaching.
  </p>

  <div class="focus-cards">
    <div class="focus-card">
      <p class="focus-card-label">Cosmological ML</p>
      <p class="focus-card-text">Displacement-field reconstruction and super-resolution of N-body simulations using neural implicit representations.</p>
    </div>
    <div class="focus-card">
      <p class="focus-card-label">Medical Imaging</p>
      <p class="focus-card-text">Accelerating MRI acquisition with wavelet scattering transforms while preserving diagnostic fidelity.</p>
    </div>
    <div class="focus-card">
      <p class="focus-card-label">Differentiable Models</p>
      <p class="focus-card-text">Simulation-based inference and neural fields for high-dimensional physical field reconstruction.</p>
    </div>
    <div class="focus-card">
      <p class="focus-card-label">Teaching</p>
      <p class="focus-card-text">Co-teaching <a href="https://diegoviillalba.github.io/almacenamienes-y-mineria-de-datos/">data mining</a> at the Facultad de Ciencias, UNAM — connecting theory with applied ML.</p>
    </div>
  </div>

  <p>
    I have developed these methods at the <a href="https://dipc.ehu.eus/" target="_blank">Donostia International Physics Center (DIPC)</a>, where I contributed to the CODECS project on cosmological simulation compression, and at the <a href="https://www.unam.mx/" target="_blank">Universidad Nacional Autónoma de México (UNAM)</a>, where my ongoing work spans astrophysical super-resolution and interpretable MRI reconstruction.
  </p>

  <p class="focus-card-label" style="margin-top:1.4rem; margin-bottom:0.6rem;">Applied domains</p>
  <div class="applications-row">
    <div class="app-card">
      <p class="app-card-title">Medical Imaging</p>
      <p class="app-card-text">Accelerating MRI acquisition while maintaining diagnostic image quality.</p>
    </div>
    <div class="app-card">
      <p class="app-card-title">Industry</p>
      <p class="app-card-text">OCR-based data processing pipelines and document intelligence systems.</p>
    </div>
  </div>
</div>

<p class="section-rule">Research Interests</p>

<div class="interests-grid">
  <div class="interest-item">Machine learning for scientific simulations</div>
  <div class="interest-item">Simulation-based inference</div>
  <div class="interest-item">Cosmological simulations & large-scale structure</div>
  <div class="interest-item">Differentiable and physics-informed modeling</div>
  <div class="interest-item">Machine learning for medical imaging</div>
  <div class="interest-item">High-performance & parallel computing</div>
  <div class="interest-item">Neural implicit representations</div>
  <div class="interest-item">Generalizable methods for real-world systems</div>
</div>

<p class="section-rule">Personal</p>

<div class="personal-block">
  <p>
    Originally from Mexico City. Alongside research, I am actively involved in <strong>teaching, mentoring, and science communication</strong>, and I enjoy helping students build strong foundations in physics and data science.
  </p>
  <p>
    I am always interested in connecting with people working on <strong>machine learning, scientific computing, or data-driven science</strong> — both in academia and industry.
  </p>
</div>

<div class="photo-block">
  <img src='/images/about_me.png' alt='Diego Villalba'>
</div>

<p class="cta-line">
  Explore my <a href="/publications/">research work</a>, <a href="/portfolio/">projects</a>, and <a href="/cv/">CV</a> — or <a href="mailto:diego.villalba@ciencias.unam.mx">reach out</a> if you'd like to collaborate.
</p>

</div>