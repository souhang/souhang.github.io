---
layout: default
title: Hang Su
---

## About Me

My name is Hang Su. I was born in Hunan, China, in July 1998 and grew up
in Guangdong. I received my Ph.D. in Physics from Shanghai Jiao Tong
University in June 2026, under the supervision of Prof. Yuan Yao.

My research focuses on quantum many-body physics and condensed matter
theory, particularly quantum magnetism, Lieb-Schultz-Mattis theorems,
and topological phases. I am also interested in quantum information,
open quantum systems, and quantum transport.

---

## Research Interests

- Quantum Magnetism and Quantum Monte Carlo Methods
- Lieb-Schultz-Mattis Theorems and Topological Phases
- Quantum Information and Open Quantum Systems
- Quantum Transport and Chiral Materials

---

## Education

**Post-Doctoral Fellow** (2026-present)  
King Fahd University of Petroleum and Minerals (KFUPM)  
Advisor: Prof. Daniel Loss & Ji Zou  

**Ph.D. in Physics** (2020–2026)  
School of Physics and Astronomy, Shanghai Jiao Tong University (SJTU)
Advisor: Prof. Yuan Yao

**B.S. in Physics** (2015–2020)  
Zhiyuan Honor College, SJTU

---

## Publications

<div class="publications" markdown="0">
{% assign previous_year = "" %}
{% for paper in site.data.publications reversed %}
{% if paper.year != previous_year %}
<h3 style="margin-top: 22px; margin-bottom: 12px; padding-bottom: 5px; border-bottom: 1px solid #e5e5e5;">
  {{ paper.year }}
</h3>
{% assign previous_year = paper.year %}
{% endif %}
<div style="display: grid; grid-template-columns: 2.2em minmax(0, 1fr); gap: 4px; margin-bottom: 12px; line-height: 1.5;">
  <div>[{{ forloop.rindex }}]</div>
  <div>
    {{ paper.authors }}<br>
    {{ paper.title }}<br>
    {% if paper.journal %}
    <a href="{{ paper.url }}"><i>{{ paper.journal }}</i> <strong>{{ paper.volume }}</strong>, {{ paper.article }} ({{ paper.year }})</a>{% if paper.arxiv %}; {% endif %}
    {% endif %}
    {% if paper.arxiv %}
    <a href="https://arxiv.org/abs/{{ paper.arxiv }}">arXiv:{{ paper.arxiv }}</a>{% unless paper.journal %} ({{ paper.year }}){% endunless %}
    {% endif %}
  </div>
</div>
{% endfor %}
<small>&#42; Equal contribution. † Corresponding authors.</small>
</div>
