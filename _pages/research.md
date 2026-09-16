---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% assign ordered_research = site.research | sort: "homepage_order" %}
{% for post in ordered_research %}
  {% include archive-single-research.html %}
{% endfor %}

