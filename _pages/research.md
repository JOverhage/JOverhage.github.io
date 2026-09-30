---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

{% include base_path %}

{% assign ordered_research = site.research | sort: "homepage_order" %}

<section class="research-index page__content" aria-label="Research papers">
  {% for paper in ordered_research %}
    {% if paper.job_market_paper %}
      <div class="research-index__featured">
        <p class="research-index__label">Job Market Paper</p>
        {% include homepage-paper.html paper=paper featured=true show_details=true download_label="Paper" %}
      </div>
    {% endif %}
  {% endfor %}

  <h2 class="research-index__section-title">Additional Research</h2>
  <div class="research-index__list">
    {% for paper in ordered_research %}
      {% unless paper.job_market_paper %}
        {% include homepage-paper.html paper=paper show_details=true download_label="Paper" %}
      {% endunless %}
    {% endfor %}
  </div>
</section>

