---
layout: page
permalink: /cv/
title: CV
nav: true
nav_order: 5
description: Curriculum Vitae
cv_pdf: /assets/pdf/sjpark_CV.pdf # you can also use external links here
cv_summary: >
  CV up-to-date for 2026.02.
---

<div class="card mt-3 mb-3">
  <div class="card-body">
    {% if page.cv_summary %}
      <p class="mb-3">{{ page.cv_summary }}</p>
    {% endif %}

    {% if page.cv_pdf %}
      <a
        {% if page.cv_pdf contains '://' %}
          href="{{ page.cv_pdf }}"
        {% else %}
          href="{{ page.cv_pdf | relative_url }}"
        {% endif %}
        target="_blank"
        rel="noopener noreferrer"
        class="btn btn-sm btn-outline-primary"
      >
        <i class="fa-solid fa-file-pdf"></i> Download PDF
      </a>
    {% endif %}
  </div>
</div>

{% if page.cv_pdf %}
  <iframe
    {% if page.cv_pdf contains '://' %}
      src="{{ page.cv_pdf }}"
    {% else %}
      src="{{ page.cv_pdf | relative_url }}"
    {% endif %}
    width="100%"
    height="1200"
    style="border: 0"
  ></iframe>
{% endif %}
