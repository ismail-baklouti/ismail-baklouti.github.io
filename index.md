---
layout: default
title: Home
---

## Biography

I am a **Research Scientist** and **Electromechanical Engineer** with over 11 years of expertise in **Decarbonization strategies** and solar energy systems. My work focuses on high-level consultancy for the design of solar thermal and fluid dynamics systems, specializing in mathematical optimization using **Pyomo** and the development of **Digital Twins**. 


## Research Axes

- **Mathematical Modeling of Solar Thermal Systems:** Development of mathematical and computational models for the design, optimization and control of solar thermal and fluid systems.
- **Robotic Kinematic Calibration:** Methods and algorithms for precise kinematic calibration of robotic manipulators to improve accuracy and repeatability.

---

## Technical Expertise

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