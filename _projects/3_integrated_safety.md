---
layout: page
title: Integrated Active and Passive Safety for Vehicles
description: Physics-informed risk assessment and multi-fidelity occupant injury prediction are integrated to bridge collision avoidance and crash injury mitigation. The proposed approach includes a physics-informed model that combines collision probability with injury severity, and a multi-fidelity learning framework that predicts occupant injury criteria from crash dynamics, restraint settings, and occupant characteristics.
img: assets/img/Research_3/research_int_safety.jpg
permalink: /projects/3_integrated_safety/
importance: 3
category: research
giscus_comments: false
related_publications: false
---

<style>
.post-header,
.post-description {
  display: none !important;
}

.research-detail-page {
  --rd-purple: #5b21b6;
  --rd-purple-dark: #351063;
  --rd-purple-soft: #f4efff;
  --rd-purple-line: #ded2f6;
  --rd-text: #202033;
  --rd-muted: #67677a;
  --rd-border: #e7e4ee;
  --rd-card: #ffffff;
  color: var(--rd-text);
}

.research-detail-page a {
  text-decoration-thickness: 1px;
  text-underline-offset: 3px;
}

/* Hero */
.research-hero {
  position: relative;
  overflow: hidden;
  min-height: 430px;
  margin: 10px 0 22px;
  border: 1px solid var(--rd-border);
  border-radius: 22px;
  background: #fff;
  /* 背景图透明度：0 = 完全透明，1 = 完全不透明 */
  --hero-img-opacity: 1;
}

/* 背景图层 */
.research-hero::before {
  content: "";
  position: absolute;
  inset: 0;
  z-index: 0;
  background: url("{{ '/assets/img/Research_3/research_int_safety.jpg' | relative_url }}") center / cover no-repeat;
  opacity: var(--hero-img-opacity);
}

/* 白色渐变遮罩层（保证左侧文字清晰） */
.research-hero::after {
  content: "";
  position: absolute;
  inset: 0;
  z-index: 1;
  background: linear-gradient(90deg,
    rgba(255,255,255,0.99) 0%,
    rgba(255,255,255,0.97) 40%,
    rgba(255,255,255,0.72) 62%,
    rgba(255,255,255,0.10) 100%);
}

.research-hero-inner {
  position: relative;
  z-index: 2;
  width: min(68%, 760px);
  padding: 66px 58px 58px;
}

.research-eyebrow {
  display: inline-flex;
  margin-bottom: 16px;
  color: var(--rd-purple);
  font-size: 13px;
  font-weight: 700;
  letter-spacing: 0.08em;
  text-transform: uppercase;
}

.research-hero h1 {
  margin: 0 0 20px;
  color: var(--rd-purple-dark);
  font-size: clamp(38px, 5vw, 62px);
  font-weight: 750;
  line-height: 1.05;
  letter-spacing: -0.035em;
}

.research-hero p {
  max-width: 720px;
  margin: 0;
  color: #3d3d4c;
  font-size: 18px;
  line-height: 1.72;
}

.research-flow {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin-top: 28px;
}

.research-flow span {
  padding: 8px 12px;
  border: 1px solid rgba(91,33,182,0.18);
  border-radius: 999px;
  background: rgba(255,255,255,0.84);
  color: var(--rd-purple-dark);
  font-size: 13px;
  font-weight: 650;
}

/* Metrics */
.research-metrics {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 16px;
  margin: 0 0 22px;
}

.metric-card {
  min-height: 118px;
  padding: 22px 24px;
  border: 1px solid var(--rd-border);
  border-radius: 16px;
  background: linear-gradient(135deg, #fff 0%, #f7f3ff 100%);
  box-shadow: 0 6px 22px rgba(42, 24, 72, 0.045);
}

.metric-value {
  margin-bottom: 5px;
  color: var(--rd-purple);
  font-size: 29px;
  font-weight: 780;
  line-height: 1;
}

.metric-title {
  margin-bottom: 5px;
  color: var(--rd-text);
  font-size: 15px;
  font-weight: 700;
}

.metric-note {
  color: var(--rd-muted);
  font-size: 13px;
  line-height: 1.5;
}

/* Sticky local navigation */
.research-subnav {
  position: sticky;
  top: 66px;
  z-index: 20;
  display: flex;
  gap: 2px;
  overflow-x: auto;
  margin: 0 0 42px;
  padding: 0 4px;
  border-bottom: 1px solid var(--rd-border);
  background: var(--global-bg-color, #fff);
  scrollbar-width: none;
}

.research-subnav::-webkit-scrollbar {
  display: none;
}

.research-subnav a {
  flex: 0 0 auto;
  padding: 15px 16px 13px;
  border-bottom: 2px solid transparent;
  color: var(--rd-muted) !important;
  font-size: 13px;
  font-weight: 650;
  text-decoration: none !important;
}

.research-subnav a:hover {
  border-bottom-color: var(--rd-purple);
  color: var(--rd-purple) !important;
}

/* Overview */
.research-overview {
  display: grid;
  grid-template-columns: minmax(150px, 0.32fr) minmax(0, 1.68fr);
  gap: 42px;
  align-items: start;
  margin-bottom: 72px;
  padding: 10px 0 48px;
  border-bottom: 1px solid var(--rd-border);
}

.overview-title {
  position: sticky;
  top: 128px;
}

.overview-kicker {
  display: inline-block;
  margin-bottom: 10px;
  color: var(--rd-purple);
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 0.08em;
  text-transform: uppercase;
}

.overview-title h2,
.resources-section h2 {
  margin: 0;
  color: var(--rd-text);
  font-size: 32px;
  font-weight: 750;
  line-height: 1.15;
  letter-spacing: -0.02em;
}

.overview-content {
  min-width: 0;
}

.overview-objective {
  margin: 0 0 20px;
  padding: 22px 24px;
  border: 1px solid var(--rd-purple-line);
  border-left: 4px solid var(--rd-purple);
  border-radius: 12px;
  background: linear-gradient(135deg, #faf7ff 0%, var(--rd-purple-soft) 100%);
  color: #393345;
  font-size: 15px;
  line-height: 1.72;
}

.overview-content p {
  max-width: 900px;
  margin: 0;
  color: var(--rd-muted);
  font-size: 16px;
  line-height: 1.8;
}

/* Research sections */
.research-section {
  scroll-margin-top: 120px;
  margin: 0 0 74px;
  padding-top: 8px;
}

.section-heading {
  display: grid;
  grid-template-columns: 64px minmax(0, 1fr);
  gap: 18px;
  align-items: start;
  margin-bottom: 26px;
}

.section-number {
  color: var(--rd-purple);
  font-family: Georgia, "Times New Roman", serif;
  font-size: 52px;
  line-height: 0.95;
}

.section-heading h2 {
  margin: 0 0 7px;
  color: var(--rd-text);
  font-size: 28px;
  font-weight: 750;
  line-height: 1.18;
  letter-spacing: -0.02em;
}

.section-heading h2 a {
  color: inherit !important;
  text-decoration: none !important;
}

.section-lead {
  margin: 0;
  color: var(--rd-muted);
  font-size: 15px;
  line-height: 1.55;
}

.section-stats {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin-top: 13px;
}

.section-stats span {
  padding: 6px 10px;
  border: 1px solid var(--rd-purple-line);
  border-radius: 999px;
  background: var(--rd-purple-soft);
  color: var(--rd-purple-dark);
  font-size: 12px;
  font-weight: 650;
}

.research-section h3 {
  margin: 30px 0 13px;
  color: var(--rd-purple-dark);
  font-size: 19px;
  font-weight: 730;
}

.research-section p,
.research-section li {
  color: var(--rd-muted);
  font-size: 15px;
  line-height: 1.72;
}

.research-section > p {
  max-width: 980px;
}

.research-section strong {
  color: var(--rd-text);
}

.research-section .row {
  margin-top: 20px !important;
  margin-bottom: 8px !important;
}

.research-section figure,
.research-section img {
  border-radius: 12px;
}

.research-section .z-depth-1 {
  box-shadow: 0 8px 24px rgba(33, 25, 48, 0.08) !important;
}

.research-section .caption {
  margin-top: 9px !important;
  color: #858394;
  font-size: 12px;
  line-height: 1.45;
  text-align: center;
}

.research-section img[src$=".gif"] {
  border: 1px solid var(--rd-border);
  background: #fff;
}


/* =========================================================
   Paper layout: compact image gallery + text
   ========================================================= */

.paper-layout {
  display: grid;
  grid-template-columns: minmax(280px, 0.78fr) minmax(0, 1.22fr);
  gap: 38px;
  align-items: start;
  margin-top: 24px;
}

.paper-layout.gallery-right {
  grid-template-columns: minmax(0, 1.22fr) minmax(280px, 0.78fr);
}

.paper-layout.gallery-right .paper-gallery {
  order: 2;
  justify-self: end;
}

.paper-layout.gallery-right .paper-copy {
  order: 1;
}

.paper-copy {
  min-width: 0;
}

.paper-copy h3:first-child {
  margin-top: 0;
}

/* Gallery stays compact and follows the text while reading */
.paper-gallery {
  width: 100%;
  max-width: 430px;
  position: sticky;
  top: 120px;
  align-self: start;
}

.gallery-main {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 300px;
  padding: 12px;
  overflow: hidden;
  border: 1px solid var(--rd-border);
  border-radius: 14px;
  background: #fff;
  box-shadow: 0 8px 24px rgba(33, 25, 48, 0.06);
}

.gallery-main img {
  display: block;
  width: 100%;
  height: 100%;
  max-width: 100%;
  max-height: 100%;
  object-fit: contain;
  object-position: center;
  border-radius: 8px;
  box-shadow: none !important;
}

.gallery-caption {
  min-height: 38px;
  margin: 9px 2px 10px;
  color: #858394;
  font-size: 11.5px;
  line-height: 1.45;
  text-align: center;
}

.gallery-thumbs {
  display: flex;
  gap: 8px;
  overflow-x: auto;
  padding: 2px 1px 5px;
  scrollbar-width: thin;
}

.gallery-thumb {
  flex: 0 0 72px;
  width: 72px;
  height: 54px;
  padding: 3px;
  overflow: hidden;
  cursor: pointer;
  border: 1px solid var(--rd-border);
  border-radius: 8px;
  background: #fff;
  opacity: 0.72;
  transition:
    opacity 0.2s ease,
    border-color 0.2s ease,
    box-shadow 0.2s ease,
    transform 0.2s ease;
}

.gallery-thumb:hover {
  opacity: 1;
  transform: translateY(-1px);
}

.gallery-thumb.active {
  opacity: 1;
  border-color: var(--rd-purple);
  box-shadow: 0 0 0 2px rgba(91, 33, 182, 0.10);
}

.gallery-thumb img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 5px;
  box-shadow: none !important;
}

/* Narrow table used only for the automation-level safety-benefit result */
.safety-benefit-table {
  width: min(100%, 680px);
  margin: 16px auto 24px;
}

.safety-benefit-table table {
  width: 100% !important;
  margin: 0 !important;
  font-size: 12.8px;
}

.safety-benefit-table th,
.safety-benefit-table td {
  padding: 9px 10px !important;
}

.safety-benefit-table th:first-child,
.safety-benefit-table td:first-child {
  white-space: nowrap;
}

/* Tablet/mobile */
@media (max-width: 900px) {
  .paper-layout,
  .paper-layout.gallery-right {
    grid-template-columns: 1fr;
    gap: 24px;
  }

  .paper-layout.gallery-right .paper-gallery,
  .paper-layout.gallery-right .paper-copy {
    order: initial;
  }

  .paper-gallery {
    position: static;
    max-width: 620px;
    justify-self: center !important;
  }

  .gallery-main {
    height: 340px;
  }
}

@media (max-width: 640px) {
  .gallery-main {
    height: 250px;
  }

  .gallery-thumb {
    flex-basis: 64px;
    width: 64px;
    height: 48px;
  }

  .safety-benefit-table {
    width: 100%;
    overflow-x: auto;
  }

  .safety-benefit-table table {
    min-width: 600px;
  }
}


/* Tables */
.research-detail-page table {
  width: 100%;
  margin: 18px 0 26px;
  overflow: hidden;
  border: 1px solid var(--rd-border);
  border-radius: 12px;
  border-collapse: separate;
  border-spacing: 0;
  background: #fff;
  font-size: 14px;
}

.research-detail-page thead th,
.research-detail-page th {
  padding: 12px 14px;
  border-bottom: 1px solid var(--rd-border);
  background: #f5f1fc;
  color: var(--rd-purple-dark);
  font-weight: 700;
}

.research-detail-page td {
  padding: 12px 14px;
  border-bottom: 1px solid #efedf3;
  color: var(--rd-muted);
  vertical-align: top;
}

.research-detail-page tr:last-child td {
  border-bottom: none;
}

/* Resources */
.resources-section {
  scroll-margin-top: 120px;
  margin-top: 34px;
  padding-top: 42px;
  border-top: 1px solid var(--rd-border);
}

.resources-intro {
  margin-bottom: 22px;
  color: var(--rd-muted);
}

.resources-section table td:first-child {
  width: 78%;
}

.resources-section table td:last-child {
  width: 22%;
  text-align: center;
}

.resources-section table a {
  font-weight: 620;
}

/* Responsive */
@media (max-width: 900px) {
  .research-hero {
    min-height: 0;
  }

  .research-hero::after {
    background: linear-gradient(rgba(255,255,255,0.93), rgba(255,255,255,0.95));
  }

  .research-hero-inner {
    width: 100%;
    padding: 46px 32px;
  }

  .research-metrics,
  .research-overview {
    grid-template-columns: 1fr;
  }

  .overview-title {
    position: static;
  }

  .research-subnav {
    top: 56px;
  }
}

@media (max-width: 640px) {
  .research-hero {
    border-radius: 14px;
  }

  .research-hero-inner {
    padding: 38px 22px;
  }

  .research-hero h1 {
    font-size: 38px;
  }

  .research-hero p {
    font-size: 16px;
  }

  .research-metrics {
    grid-template-columns: 1fr;
  }

  .section-heading {
    grid-template-columns: 48px minmax(0, 1fr);
    gap: 12px;
  }

  .section-number {
    font-size: 42px;
  }

  .section-heading h2 {
    font-size: 23px;
  }

  .research-detail-page table {
    display: block;
    overflow-x: auto;
  }
}

/* Keep this page's resource table spacing consistent with its reference layout. */
.research-detail-page .resources-section table th,
.research-detail-page .resources-section table td {
  padding: 12px 14px;
  font-size: 14px;
  border-top: 0;
}
</style>

<div class="research-detail-page">

<section class="research-hero" aria-labelledby="integrated-safety-title">
  <div class="research-hero-inner">
    <div class="research-eyebrow">Autonomous vehicle safety research</div>
    <h1 id="integrated-safety-title">Integrated Safety</h1>
    <p>
      We connect pre-crash collision risk with potential injury consequences and
      develop data-efficient models of occupant response. Through physics-informed
      risk assessment and knowledge-guided multi-fidelity learning, our research
      supports the coordination of active collision avoidance and passive occupant protection.
    </p>
    <div class="research-flow">
      <span>Integrated Safety</span>
      <span>Occupant injury mitigation</span>
      <span>Multi-fidelity learning</span>
      <span>Active and passive safety</span>
    </div>
  </div>
</section>

<div class="research-metrics">
  <div class="metric-card">
    <div class="metric-value">1,879</div>
    <div class="metric-title">Safety-critical driving events</div>
    <div class="metric-note">12 participants encountered cut-in, merging, and braking conflicts in simulator experiments.</div>
  </div>
  <div class="metric-card">
    <div class="metric-value">8.0%</div>
    <div class="metric-title">Lower integrated-risk MAE</div>
    <div class="metric-note">PIRAM versus GRU on the study's test split: IDR MAE decreased from 3.577 to 3.291.</div>
  </div>
  <div class="metric-card">
    <div class="metric-value">17.6%</div>
    <div class="metric-title">Lower injury-prediction MAE</div>
    <div class="metric-note">Average relative reduction across three injury criteria versus HF-only at 500 HF cases, with auxiliary LF data.</div>
  </div>
</div>

<nav class="research-subnav" aria-label="Integrated safety page sections">
  <a href="#overview">Overview</a>
  <a href="#integrated-driving-risk">Integrated Risk</a>
  <a href="#multi-fidelity-injury">Injury Prediction</a>
  <a href="#publications-data">Publications &amp; Resources</a>
</nav>

<section id="overview" class="research-overview" aria-labelledby="objective-title">
  <div class="overview-title">
    <span class="overview-kicker">Research framework</span>
    <h2 id="objective-title">Objective</h2>
  </div>
  <div class="overview-content">
    <div class="overview-objective">
      <strong>Integrated vehicle safety links the likelihood of a collision to its potential consequences for occupants.</strong>
      We investigate two complementary components of this challenge: a physics-informed model that combines
      collision probability with injury-related severity, and a multi-fidelity learning framework that predicts
      occupant injury criteria from crash dynamics, restraint settings, and occupant characteristics.
      These research directions provide a quantitative basis for linking pre-crash risk assessment with crash
      protection, while reducing dependence on costly high-fidelity simulation data.
    </div>
  </div>
</section>


<section id="integrated-driving-risk" class="research-section" markdown="1">

<div class="section-heading">
  <div class="section-number">01</div>
  <div>
    <h2><a href="https://doi.org/10.1016/j.aap.2025.108266">Physics-informed integrated driving risk assessment</a></h2>
    <p class="section-lead">Combine collision probability and potential injury-related consequences to support timely occupant protection.</p>
    <div class="section-stats">
      <span>12 participants</span>
      <span>1,879 safety-critical events</span>
      <span>8.0% lower IDR MAE vs. GRU</span>
      <span>Physics-informed attention</span>
    </div>
  </div>
</div>

<div class="paper-layout gallery-right">

  <aside class="paper-gallery" data-gallery="lu-2025-aap">
    <div class="gallery-main">
      <img src="{{ '/assets/img/Research_3/paper_lu_2025_piram_framework.jpg' | relative_url }}" alt="Physics-informed training framework of PIRAM (Fig. 4).">
    </div>
    <div class="gallery-caption">Physics-informed training framework of PIRAM (Fig. 4).</div>
    <div class="gallery-thumbs">
      <button type="button" class="gallery-thumb active"
        data-src="{{ '/assets/img/Research_3/paper_lu_2025_piram_framework.jpg' | relative_url }}"
        data-caption="Physics-informed training framework of PIRAM (Fig. 4)."
        aria-label="Show Physics-informed training framework of PIRAM (Fig. 4).">
        <img src="{{ '/assets/img/Research_3/paper_lu_2025_piram_framework.jpg' | relative_url }}" alt="">
      </button>
      <button type="button" class="gallery-thumb"
        data-src="{{ '/assets/img/Research_3/paper_lu_2025_piram_dataset.jpg' | relative_url }}"
        data-caption="Simulator-based data collection across cut-in, merging, and braking conflicts (Fig. 1)."
        aria-label="Show Simulator-based data collection across cut-in, merging, and braking conflicts (Fig. 1).">
        <img src="{{ '/assets/img/Research_3/paper_lu_2025_piram_dataset.jpg' | relative_url }}" alt="">
      </button>
      <button type="button" class="gallery-thumb"
        data-src="{{ '/assets/img/Research_3/paper_lu_2025_piram_risk_metric.jpg' | relative_url }}"
        data-caption="Integrated driving risk combines collision probability with injury-related severity (Fig. 5)."
        aria-label="Show Integrated driving risk combines collision probability with injury-related severity (Fig. 5).">
        <img src="{{ '/assets/img/Research_3/paper_lu_2025_piram_risk_metric.jpg' | relative_url }}" alt="">
      </button>
      <button type="button" class="gallery-thumb"
        data-src="{{ '/assets/img/Research_3/paper_lu_2025_piram_case_result.jpg' | relative_url }}"
        data-caption="Risk evolution in one reconstructed CIDAS collision: the Level III threshold is reached 0.45 s earlier than TTC (Fig. 8)."
        aria-label="Show Risk evolution in one reconstructed CIDAS collision: the Level III threshold is reached 0.45 s earlier than TTC (Fig. 8).">
        <img src="{{ '/assets/img/Research_3/paper_lu_2025_piram_case_result.jpg' | relative_url }}" alt="">
      </button>
    </div>
  </aside>

  <div class="paper-copy" markdown="1">

### 1.1 Framework

Avoiding a collision and limiting its consequences require a shared understanding of driving risk. Collision likelihood alone cannot distinguish a low-impact conflict from a potentially severe crash. We developed a **physics-informed integrated risk assessment model (PIRAM)** that combines collision probability and potential severity in a unified **integrated driving risk (IDR)** metric. By connecting vehicle interactions with injury-related consequences, the framework provides a quantitative basis for coordinating pre-crash warnings and occupant protection.

### 1.2 Dataset

The **integrated driving risk prediction dataset (IDRPD)** was collected using a high-fidelity motion simulator and CARLA-based traffic scenarios. **Twelve participants** responded to cut-in, merging, and emergency-braking conflicts, yielding **1,879 safety-critical events** after data cleaning. Vehicle interactions were recorded at **20 Hz**. Sliding time windows produced **12,436 augmented input sequences** from these events, covering normal driving and evolving pre-collision or collision-avoidance interactions. Windows containing the collision instant were excluded. Quantitative comparisons used the study's **80%/20% training/test split**.

### 1.3 Methods

An attention-based neural network encodes vehicle motion histories and local map information to capture interactions among surrounding vehicles and road geometry. A parallel **dynamic bicycle model** evaluates physically plausible future maneuvers and guides neural-network training through adaptively weighted prediction losses. This combines data-driven representation learning with vehicle-dynamics knowledge.

The model predicts collision-time categories and collision-velocity-based severity categories. Collision probabilities are combined with injury-risk curves and severity-related economic losses to construct IDR. The resulting metric accounts for both the likelihood and potential consequences of a collision. Severity is quantified using a **collision-speed-based proxy informed by population-level injury statistics**.

### 1.4 Results

On the IDRPD evaluation split, PIRAM achieved **81.4% collision-time classification accuracy** and **95.1% severity-category accuracy**. For the final IDR metric, MAE decreased from **3.577 to 3.291**, an **8.0% reduction relative to GRU**, the strongest baseline on this measure; Spearman's rank correlation increased from **0.769 to 0.811**. These results indicate more accurate estimation and ordering of risk across the evaluated interactions.

In **one reconstructed CIDAS intersection collision**, PIRAM reached the Level III protection threshold approximately **0.45 s earlier** than the TTC-based comparison. This reconstructed case illustrates how injury-aware risk estimation can support earlier protection decisions, complementing the simulator-based evaluation.

  </div>

</div>

</section>


<section id="multi-fidelity-injury" class="research-section" markdown="1">

<div class="section-heading">
  <div class="section-number">02</div>
  <div>
    <h2><a href="https://doi.org/10.1016/j.aei.2026.105117">Knowledge-guided multi-fidelity injury prediction</a></h2>
    <p class="section-lead">Use knowledge from low-cost crash simulations to predict occupant injuries when high-fidelity training data are scarce.</p>
    <div class="section-stats">
      <span>4,849 LF simulations</span>
      <span>3,598 HF simulations</span>
      <span>17.6% lower MAE on average at 500 HF</span>
      <span>Unpaired multi-fidelity learning</span>
    </div>
  </div>
</div>

<div class="paper-layout">

  <aside class="paper-gallery" data-gallery="lu-2026-aei">
    <div class="gallery-main">
      <img src="{{ '/assets/img/Research_3/paper_lu_2026_mfpgrnet_framework.jpg' | relative_url }}" alt="MF-PGRNet combines low-fidelity physics priors with high-fidelity residual correction (Fig. 2).">
    </div>
    <div class="gallery-caption">MF-PGRNet combines low-fidelity physics priors with high-fidelity residual correction (Fig. 2).</div>
    <div class="gallery-thumbs">
      <button type="button" class="gallery-thumb active"
        data-src="{{ '/assets/img/Research_3/paper_lu_2026_mfpgrnet_framework.jpg' | relative_url }}"
        data-caption="MF-PGRNet combines low-fidelity physics priors with high-fidelity residual correction (Fig. 2)."
        aria-label="Show MF-PGRNet combines low-fidelity physics priors with high-fidelity residual correction (Fig. 2).">
        <img src="{{ '/assets/img/Research_3/paper_lu_2026_mfpgrnet_framework.jpg' | relative_url }}" alt="">
      </button>
      <button type="button" class="gallery-thumb"
        data-src="{{ '/assets/img/Research_3/paper_lu_2026_mfpgrnet_dataset.jpg' | relative_url }}"
        data-caption="Rear-end collision configuration and occupant, restraint, and injury variables in the high-fidelity dataset (Fig. 1)."
        aria-label="Show Rear-end collision configuration and occupant, restraint, and injury variables in the high-fidelity dataset (Fig. 1).">
        <img src="{{ '/assets/img/Research_3/paper_lu_2026_mfpgrnet_dataset.jpg' | relative_url }}" alt="">
      </button>
      <button type="button" class="gallery-thumb"
        data-src="{{ '/assets/img/Research_3/paper_lu_2026_mfpgrnet_sample_efficiency.jpg' | relative_url }}"
        data-caption="Test MAE and R-squared across high-fidelity training-set sizes for head, neck, and chest injury criteria (Fig. 4)."
        aria-label="Show Test MAE and R-squared across high-fidelity training-set sizes for head, neck, and chest injury criteria (Fig. 4).">
        <img src="{{ '/assets/img/Research_3/paper_lu_2026_mfpgrnet_sample_efficiency.jpg' | relative_url }}" alt="">
      </button>
    </div>
  </aside>

  <div class="paper-copy" markdown="1">

### 2.1 Framework

Accurate occupant injury prediction supports restraint-system design and virtual safety assessment, but high-fidelity crash simulations are expensive to generate. Low-fidelity simulations offer accessible crash-response knowledge, while their simplified mechanics introduce systematic biases. Independently generated datasets also lack one-to-one correspondence. We developed **MF-PGRNet**, a knowledge-guided multi-fidelity residual learning framework that uses low-fidelity simulations as structured physics priors. It combines reusable injury-response trends with corrections learned from limited high-fidelity data, improving prediction **without requiring paired simulations**.

### 2.2 Dataset

The study combines **4,849 low-fidelity (LF) simulations**, generated using Visual Crash Studio and MADYMO, with **3,598 high-fidelity (HF) finite-element rear-end collision cases** generated using LS-DYNA. The HF simulations assess occupants in the following vehicle across variations in collision configuration, restraint settings, body size, and sitting posture. Each HF case required approximately **45 hours on 24 CPU cores**. A fixed set of **598 HF cases** was reserved for testing, with a training pool of 3,000 cases. The sample-efficiency experiment used **4,000 LF cases** and HF subsets of 200 to 3,000 cases, with five random subsamplings at each size.

### 2.3 Methods

The model jointly encodes longitudinal and lateral crash pulses, restraint parameters, and occupant characteristics. A **learnable prototype library** summarizes characteristic patterns in the LF dataset, and cross-attention retrieves relevant priors for each HF query. Predictions combine an **LF-derived trend and an HF-specific residual correction**, with adaptive gating balancing observed features and retrieved knowledge. **Relational knowledge distillation** preserves relative relationships among scenarios to stabilize learning when HF data are scarce. Outputs include the head injury criterion (**HIC**), normalized neck injury criterion (**N<sub>ij</sub>**), and maximum chest deflection (**D<sub>max</sub>**); injury-risk curves translate these continuous predictions into AIS severity categories.

### 2.4 Results

With **500 HF training cases**, MF-PGRNet reduced MAE by an average of **17.6% across the three injury criteria** relative to the HF-only baseline. The reductions were **17.3%, 11.4%, and 24.1%** for HIC, N<sub>ij</sub>, and D<sub>max</sub>, respectively. For HIC prediction, its MAE with 500 HF cases was **78.34**, compared with **82.85** for HF-only trained on 1,000 cases, demonstrating better mean accuracy with half as many HF labels in this comparison.

With **200 HF training cases**, three-category head-injury classification reached **85.5% accuracy**, compared with **81.6%** for HF-only, on the fixed simulation test set. These results support data-efficient virtual safety assessment and occupant protection design. A supplementary assessment using **789 frontal-impact field-crash records** provided preliminary evidence of transfer beyond the rear-end simulation matrix; broader physical-test and cross-platform validation remains necessary.

  </div>

</div>

</section>


<section id="publications-data" class="resources-section" markdown="1">

## Publications & Resources

| Paper | Data Availability |
| :--- | :---: |
| [**Lu, T., et al.** (2025). A physics-informed attention model for integrated driving risk assessment. *Accident Analysis & Prevention, 223*, 108266. https://doi.org/10.1016/j.aap.2025.108266](https://doi.org/10.1016/j.aap.2025.108266) | Data available on request |
| [**Lu, T., et al.** (2026). A knowledge-guided multi-fidelity residual learning framework for occupant injury prediction from crash simulations. *Advanced Engineering Informatics, 76*, 105117. https://doi.org/10.1016/j.aei.2026.105117](https://doi.org/10.1016/j.aei.2026.105117) | Data available on request |

</section>

<script>
document.addEventListener("DOMContentLoaded", function () {
  document.querySelectorAll(".paper-gallery").forEach(function (gallery) {
    const mainImage = gallery.querySelector(".gallery-main img");
    const caption = gallery.querySelector(".gallery-caption");
    const thumbs = gallery.querySelectorAll(".gallery-thumb");

    thumbs.forEach(function (thumb) {
      thumb.addEventListener("click", function () {
        const nextSrc = thumb.dataset.src;
        const nextCaption = thumb.dataset.caption || "";

        if (nextSrc) {
          mainImage.src = nextSrc;
          mainImage.alt = nextCaption;
        }

        caption.textContent = nextCaption;

        thumbs.forEach(function (item) {
          item.classList.remove("active");
        });

        thumb.classList.add("active");
      });
    });
  });
});
</script>

</div>
