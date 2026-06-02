---
layout: default
title: Impact
description: "Documented business impact from credit risk, ML, and data science work across Zurich North America, Discover Financial Services, EXL Services, and DIMTS."
---

<div class="page-hero">
  <div class="container">
    <h1>Impact & Achievements</h1>
    <p class="page-hero__sub">
      Quantified outcomes from {{ site.data.profile.years_experience }} years in financial services.
      All metrics sourced from direct role contributions.
    </p>
  </div>
</div>

<section class="section">
  <div class="container">

    <div class="section__header">
      <h2 class="section__title">Zurich North America</h2>
      <p class="section__subtitle">Data &amp; Applied Scientist · Aug 2024 – Present</p>
    </div>

    <div class="achievements-grid">
      {% for achievement in site.data.achievements %}
        {% if achievement.employer == "Zurich North America" %}
        <div class="achievement-row">
          <div>
            <div class="achievement-row__metric">{{ achievement.metric }}</div>
            <span class="tag tag--resume">resume-sourced</span>
          </div>
          <div class="achievement-row__context">{{ achievement.context }}</div>
          <div>
            <div class="achievement-row__employer">{{ achievement.employer }}</div>
            <div class="achievement-row__period">{{ achievement.period }}</div>
          </div>
        </div>
        {% endif %}
      {% endfor %}
    </div>

  </div>
</section>

<section class="section section--alt">
  <div class="container">

    <div class="section__header">
      <h2 class="section__title">Discover Financial Services</h2>
      <p class="section__subtitle">Lead Data Science Analyst · May 2022 – Aug 2024</p>
    </div>

    <div class="achievements-grid">
      {% for achievement in site.data.achievements %}
        {% if achievement.employer == "Discover Financial Services" %}
        <div class="achievement-row">
          <div>
            <div class="achievement-row__metric">{{ achievement.metric }}</div>
            <span class="tag tag--resume">resume-sourced</span>
          </div>
          <div class="achievement-row__context">{{ achievement.context }}</div>
          <div>
            <div class="achievement-row__employer">{{ achievement.employer }}</div>
            <div class="achievement-row__period">{{ achievement.period }}</div>
          </div>
        </div>
        {% endif %}
      {% endfor %}
    </div>

  </div>
</section>

<section class="section">
  <div class="container">

    <div class="section__header">
      <h2 class="section__title">Earlier Roles</h2>
      <p class="section__subtitle">EXL Services (CVS &amp; Aetna Health) · DIMTS Ltd.</p>
    </div>

    <div class="achievements-grid">
      {% for achievement in site.data.achievements %}
        {% unless achievement.employer == "Zurich North America" or achievement.employer == "Discover Financial Services" %}
        <div class="achievement-row">
          <div>
            <div class="achievement-row__metric">{{ achievement.metric }}</div>
            <span class="tag tag--resume">resume-sourced</span>
          </div>
          <div class="achievement-row__context">{{ achievement.context }}</div>
          <div>
            <div class="achievement-row__employer">{{ achievement.employer }}</div>
            <div class="achievement-row__period">{{ achievement.period }}</div>
          </div>
        </div>
        {% endunless %}
      {% endfor %}
    </div>

  </div>
</section>
