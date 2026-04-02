---
layout: default
title: About
permalink: /about/
---

# {{ site.title }}

{{ site.description }}

## Bio

Add a short professional biography here. Mention your research interests, current role, and notable affiliations.

## Contact

- Email (personal):
	{% if site.email %}
	{% assign email_subject = "Contact: Inquiry" | uri_escape %}
	{% assign email_body = "Hello Dr. Baklouti, I am contacting you regarding..." | uri_escape %}
	- <a href="mailto:{{ site.email }}?subject={{ email_subject }}&body={{ email_body }}" title="Email {{ site.email }}">{{ site.email }}</a>
	{% else %}
	- <span class="disabled-link">Not available</span>
	{% endif %}
- Email (work): <a href="mailto:{{ site.alt_email }}">{{ site.alt_email }}</a>
- Email (work):
	{% if site.alt_email %}
	{% assign work_subject = "Contact: Work Inquiry" | uri_escape %}
	{% assign work_body = "Hello Dr. Baklouti, I am contacting you regarding a work-related matter..." | uri_escape %}
	- <a href="mailto:{{ site.alt_email }}?subject={{ work_subject }}&body={{ work_body }}" title="Email {{ site.alt_email }}">{{ site.alt_email }}</a>
	{% else %}
	- <span class="disabled-link">Not available</span>
	{% endif %}
- ORCID: <a href="https://orcid.org/0000-0002-6847-9017" target="_blank">0000-0002-6847-9017</a>
- Google Scholar: <a href="https://scholar.google.com/citations?user=Af0tawMAAAAJ" target="_blank">Profile</a>

Feel free to edit this page to add more details, publications, and a photo (assets/img/prof_pic.jpg).