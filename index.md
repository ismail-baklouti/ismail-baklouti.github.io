---
layout: default
title: Home
---

## Biography

I am a **Research Scientist** specializing in decarbonization engineering strategies via advanced Computational Modeling. My academic background includes a degree in **Electromechanical Engineering** (2011), a **Research Master’s in Mechanical Engineering** (2012), and a **PhD in Energy Engineering** (2021). 

With over a decade of experience in research and technical consulting, my work focuses on the design, optimization, and control of complex mechanical and thermal energy systems. I specialize in developing **Digital Twins** and solving mathematical optimization problems using advanced programming tools, particularly **Python (Pyomo)** and **Julia (JuMP)**.

---

## Research Areas

*   **Mathematical Modeling of Thermal Energy Systems:** Developing computational and mathematical models for the design, optimization, and control of thermal, fluid, and mechanical energy systems.
*   **Robotic Kinematic Calibration:** Designing precise algorithms and methodology for the kinematic calibration of robotic manipulators to enhance accuracy and repeatability.

---

## Technical Expertise

My technical focus centers on mathematical programming, scientific computing, and energy system simulation, with a primary emphasis on **Python (Pyomo)** and **Julia (JuMP)**.

<div class="skill-container">
{% for skill in site.data.skills %}
  {% for tool in skill.tools %}
    <span class="skill-tag">{{ tool }}</span>
  {% endfor %}
{% endfor %}
</div>

---

## Publications

{% assign publications_by_year = site.data.publications | group_by: "year" %}
{% for year in publications_by_year %}
<div class="year-group">{{ year.name }}</div>
{% for pub in year.items %}
<div class="pub-card">
  <span class="pub-title">{{ pub.title }}</span>
  <span class="pub-authors">
    {% if pub.authors contains "I. Baklouti" %}
      {{ pub.authors | replace: "I. Baklouti", "<strong>I. Baklouti</strong>" }}
    {% else %}
      {{ pub.authors }}
    {% endif %}
  </span>
  <span class="pub-venue">{{ pub.journal }}</span>
  <a href="{{ pub.link }}" target="_blank" class="doi-btn">
    <i class="fas fa-external-link-alt"></i> View Paper
  </a>
</div>
{% endfor %}
{% endfor %}
