---
permalink: /
title: "Main Page"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---


I am a PhD candidate at the Institute for International Economic Studies, Stockholm University. My interests lie in Macro- and Monetary Economics broadly. In particular, I study the role of imperfect information and imperfect markets. 

I am on the 2026/27 Academic Job Market.

{% assign homepage_papers = site.research | where: "show_on_home", true | sort: "homepage_order" %}

<section class="homepage-research" aria-label="Research">
  {% for paper in homepage_papers %}
    {% if paper.job_market_paper %}
      <div class="homepage-research__jmp">
        <p class="homepage-research__label">Job Market Paper</p>
        {% include homepage-paper.html paper=paper featured=true %}
      </div>
    {% endif %}
  {% endfor %}

  <h2 class="homepage-research__heading">Additional Research</h2>
  <div class="homepage-research__additional">
    {% for paper in homepage_papers %}
      {% unless paper.job_market_paper %}
        {% include homepage-paper.html paper=paper %}
      {% endunless %}
    {% endfor %}
  </div>
</section>



<!--
## [Teaching](teaching)


## [CV](cv)
-->

<!--
git commit -am "add change to ________" && git push
-->

<!--
git add _pages/about.md && git commit -m "add change to _pages/about" && git push
-->
