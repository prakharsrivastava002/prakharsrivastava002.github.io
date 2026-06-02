---
layout: default
title: Publications
description: "Peer-reviewed and preprint research by Prakhar Srivastava in ML, NLP, time-series forecasting, and reinforcement learning."
---

<div class="page-hero">
  <div class="container">
    <h1>Publications</h1>
    <p class="page-hero__sub">
      {{ site.data.publications | size }} publications in ML, NLP, and applied AI.
      All entries independently verified via DOI or public URL.
      Citation counts not listed — Google Scholar profile unreachable at time of audit.
    </p>
  </div>
</div>

<section class="section">
  <div class="container">

    <div class="pub-list">
      {% for pub in site.data.publications %}
      <div class="pub-card">

        <div class="pub-card__title">{{ pub.title }}</div>

        <div class="pub-card__meta">
          <span class="pub-card__venue">{{ pub.venue }}</span>
          <span class="pub-card__sep">·</span>
          <span class="pub-card__year">
            {% if pub.year %}{{ pub.year }}{% else %}year TBC{% endif %}
          </span>
          {% if pub.verification_status == "verified_public" %}
          <span class="badge badge--verified">verified public</span>
          {% endif %}
        </div>

        {% if pub.authors.size > 0 %}
        <div class="pub-card__authors">{{ pub.authors | join: ", " }}</div>
        {% else %}
        <div class="pub-card__authors" style="font-style:italic;color:var(--gray-500)">Author list requires institutional access</div>
        {% endif %}

        {% if pub.conference %}
        <div class="pub-card__authors">Presented at: {{ pub.conference }}</div>
        {% endif %}

        <div class="pub-card__footer">
          {% if pub.doi %}
          <a class="pub-card__link" href="https://doi.org/{{ pub.doi }}" target="_blank" rel="noopener">
            DOI: {{ pub.doi }} ↗
          </a>
          {% endif %}
          {% if pub.arxiv %}
          <a class="pub-card__link" href="https://arxiv.org/abs/{{ pub.arxiv }}" target="_blank" rel="noopener">
            arXiv:{{ pub.arxiv }} ↗
          </a>
          {% endif %}
          {% if pub.ieee_doc %}
          <a class="pub-card__link" href="{{ pub.url }}" target="_blank" rel="noopener">
            IEEE Xplore: {{ pub.ieee_doc }} ↗
          </a>
          {% endif %}
          {% if pub.note %}
          <span class="pub-card__note">{{ pub.note }}</span>
          {% endif %}
        </div>

      </div>
      {% endfor %}
    </div>

  </div>
</section>

<section class="section section--alt">
  <div class="container">
    <div class="section__header">
      <h2 class="section__title">Verification Notes</h2>
    </div>
    <ul style="display:flex;flex-direction:column;gap:0.6rem;font-size:0.875rem;color:var(--text-muted);">
      <li>✔ All four publications confirmed via public DOI or URL.</li>
      <li>✔ Co-authors listed where publicly available without institutional login.</li>
      <li>✘ Citation counts omitted — Google Scholar redirects to login; no public count source available.</li>
      <li>✘ IEEE Xplore paper year and full author list require IEEE authentication to access.</li>
    </ul>
  </div>
</section>
