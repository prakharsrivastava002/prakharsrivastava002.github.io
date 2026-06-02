---
layout: default
title: Home
description: "Senior Data Scientist with 6+ years in financial services. Specializing in credit risk analytics, ML, and causal inference."
---

<!-- ============================================================
     HERO
     ============================================================ -->
<section class="hero">
  <div class="container">

    <p class="hero__meta">
      {{ site.data.profile.location }}
      &nbsp;·&nbsp;
      <a href="mailto:{{ site.data.profile.email }}">{{ site.data.profile.email }}</a>
    </p>

    <div class="hero__name-row">
      <h1>{{ site.data.profile.name }}</h1>
      {% for award in site.data.awards %}{% if award.highlight %}<span class="badge badge--o1a" title="{{ award.significance }}">{{ award.title | split: " " | slice: 0, 2 | join: " " }}</span>{% endif %}{% endfor %}
    </div>

    <p class="hero__headline">{{ site.data.profile.headline }}</p>

    <p class="hero__summary">
      {{ site.data.profile.years_experience }} years building credit risk and ML models with direct P&amp;L accountability
      in financial services. Aggregate documented impact:
      $198M exposure reduction · $11M PBT benefit · $2.03B portfolio risk improvement.
    </p>

    <div class="hero__actions">
      <a href="{{ '/publications/' | relative_url }}" class="btn btn--primary">Publications →</a>
      <a href="{{ '/achievements/' | relative_url }}" class="btn btn--ghost">View Impact</a>
    </div>

  </div>
</section>

<!-- ============================================================
     SELECTED IMPACT
     ============================================================ -->
<section class="section">
  <div class="container">
    <div class="section__header">
      <h2 class="section__title">Selected Impact</h2>
      <p class="section__subtitle">Key business outcomes from credit risk and ML work at Zurich North America and Discover Financial Services.</p>
    </div>

    <div class="stat-grid">
      {% for achievement in site.data.achievements limit:4 %}
      <div class="stat-card">
        <div class="stat-card__metric">{{ achievement.metric }}</div>
        <div class="stat-card__context">{{ achievement.context }}</div>
        <div class="stat-card__employer">{{ achievement.employer }} · {{ achievement.period }}</div>
      </div>
      {% endfor %}
    </div>

    <div class="section__cta">
      <a href="{{ '/achievements/' | relative_url }}" class="btn btn--outline">See all impact metrics →</a>
    </div>
  </div>
</section>

<!-- ============================================================
     PUBLICATIONS
     ============================================================ -->
<section class="section section--alt">
  <div class="container">
    <div class="section__header">
      <h2 class="section__title">Publications</h2>
      <p class="section__subtitle">Peer-reviewed and preprint research in ML, NLP, and applied AI.</p>
    </div>

    <div class="pub-list">
      {% for pub in site.data.publications %}
      <div class="pub-card">
        <div class="pub-card__title">{{ pub.title }}</div>

        <div class="pub-card__meta">
          <span class="pub-card__venue">{{ pub.venue }}</span>
          <span class="pub-card__sep">·</span>
          <span class="pub-card__year">{% if pub.year %}{{ pub.year }}{% else %}forthcoming{% endif %}</span>
          <span class="badge badge--verified">verified</span>
        </div>

        {% if pub.authors.size > 0 %}
        <div class="pub-card__authors">{{ pub.authors | join: ", " }}</div>
        {% endif %}

        <div class="pub-card__footer">
          {% if pub.doi %}
          <a class="pub-card__link" href="https://doi.org/{{ pub.doi }}" target="_blank" rel="noopener">DOI ↗</a>
          {% elsif pub.url %}
          <a class="pub-card__link" href="{{ pub.url }}" target="_blank" rel="noopener">View paper ↗</a>
          {% endif %}
          {% if pub.arxiv %}
          <a class="pub-card__link" href="https://arxiv.org/abs/{{ pub.arxiv }}" target="_blank" rel="noopener">arXiv:{{ pub.arxiv }} ↗</a>
          {% endif %}
          {% if pub.note %}
          <span class="pub-card__note">{{ pub.note }}</span>
          {% endif %}
        </div>
      </div>
      {% endfor %}
    </div>

    <div class="section__cta">
      <a href="{{ '/publications/' | relative_url }}" class="btn btn--outline">Full publication details →</a>
    </div>
  </div>
</section>

<!-- ============================================================
     RECOGNITION
     ============================================================ -->
<section class="section">
  <div class="container">
    <div class="section__header">
      <h2 class="section__title">Recognition</h2>
    </div>

    <div class="award-list">
      {% for award in site.data.awards %}
      <div class="award-item{% if award.highlight %} award-item--highlight{% endif %}">
        <div class="award-item__icon">{% if award.highlight %}✦{% else %}◆{% endif %}</div>
        <div class="award-item__body">
          <div class="award-item__title">{{ award.title }}</div>
          <div class="award-item__detail">
            {{ award.issuer }}{% if award.period %} · {{ award.period }}{% endif %}{% if award.date %} · {{ award.date }}{% endif %}{% if award.note %} · {{ award.note }}{% endif %}
          </div>
          {% if award.significance %}
          <div class="award-item__sig">{{ award.significance }}</div>
          {% endif %}
        </div>
      </div>
      {% endfor %}
    </div>
  </div>
</section>

<!-- ============================================================
     EXPERIENCE SNAPSHOT
     ============================================================ -->
<section class="section section--alt">
  <div class="container">
    <div class="section__header">
      <h2 class="section__title">Experience</h2>
    </div>

    <div class="timeline">
      {% for role in site.data.profile.experience %}
      <div class="timeline-item">
        <div class="timeline-item__dot"></div>
        <div class="timeline-item__body">
          <div class="timeline-item__title">{{ role.title }}</div>
          <div class="timeline-item__company">{{ role.company }}</div>
          <div class="timeline-item__meta">
            {{ role.location }}
            &nbsp;·&nbsp;
            {{ role.start | replace: "-", "/" }}
            –
            {% if role.end == "present" %}Present{% else %}{{ role.end | replace: "-", "/" }}{% endif %}
            {% if role.client %}&nbsp;· Client: {{ role.client }}{% endif %}
          </div>
        </div>
      </div>
      {% endfor %}
    </div>

    <div style="margin-top:2rem;">
      <div class="section__header" style="margin-bottom:1.25rem;">
        <h2 class="section__title" style="font-size:1.1rem;">Education</h2>
      </div>
      <div class="timeline">
        {% for edu in site.data.profile.education %}
        <div class="timeline-item">
          <div class="timeline-item__dot"></div>
          <div class="timeline-item__body">
            <div class="timeline-item__title">{{ edu.degree }}</div>
            <div class="timeline-item__company">{{ edu.school }}</div>
            <div class="timeline-item__meta">
              {{ edu.location }}
              &nbsp;·&nbsp;
              {{ edu.start | replace: "-", "/" }} – {{ edu.end | replace: "-", "/" }}
              {% if edu.honor %}&nbsp;· {{ edu.honor }}{% endif %}
            </div>
          </div>
        </div>
        {% endfor %}
      </div>
    </div>
  </div>
</section>

<!-- ============================================================
     CONTACT
     ============================================================ -->
<section class="contact" id="contact">
  <div class="container">
    <h2>Get in Touch</h2>
    <p class="contact__sub">Open to senior data science, applied ML, and risk analytics opportunities.</p>
    <a href="mailto:{{ site.data.profile.email }}" class="contact__email">{{ site.data.profile.email }}</a>
    <br>
    <a href="mailto:{{ site.data.profile.email }}" class="btn btn--primary">Send an email →</a>
  </div>
</section>
