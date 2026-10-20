---
permalink: /
excerpt: "Jonas Overhage is a macroeconomist and PhD candidate at IIES, Stockholm University, on the 2026–27 academic job market."
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---


I am a PhD candidate at the Institute for International Economic Studies (IIES), Stockholm University. I am on the 2026–27 academic job market. I study how imperfect information and imperfect markets influence individual behavior and macroeconomic outcomes.

My research combines quantitative macroeconomic models with microeconomic evidence, especially survey data. My job market paper studies how households infer aggregate conditions from their own cash flows, develops a numerical method for solving heterogeneous-agent models with dispersed information, and quantifies how this inference changes the effects of fiscal transfers.

**Fields:** Macroeconomics, Monetary Economics, Firm Dynamics

**Research interests:** Information, household behavior and expectations, market power

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
