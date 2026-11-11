---
title: Curriculum vitae
permalink: /cv/
description: Academic background and teaching experience of Mohammad Naderitabar, PhD candidate in Economics at Stockholm University.
redirect_from:
  - /resume/
---

{% if site.cv_pdf %}
<p class="page-intro"><a class="download-link" href="{{ site.cv_pdf | relative_url }}">Download CV (PDF) <span aria-hidden="true">↓</span></a></p>
{% else %}
<p class="page-intro">For a current copy of my CV, please <a href="mailto:{{ site.author.email }}?subject=CV%20request">contact me by email</a>.</p>
{% endif %}

<section class="content-section first-section" aria-labelledby="education-heading">
  <h2 id="education-heading">Education</h2>
  <div class="cv-entry">
    <h3>PhD in Economics</h3>
    <p>PhD candidate · Stockholm University<br>Institute for International Economic Studies (IIES)</p>
  </div>
</section>
<section class="content-section" aria-labelledby="fields-heading">
  <h2 id="fields-heading">Research interests</h2>
  <p>Macroeconomics, industrial organization, innovation, and information economics.</p>
</section>
<section class="content-section" aria-labelledby="teaching-heading">
  <h2 id="teaching-heading">Teaching experience</h2>
  {% for course in site.data.teaching.courses %}
  <div class="cv-entry">
    <h3>{{ course.title }}</h3>
    <p>{{ course.role }} · {{ course.level }} · {{ course.institution }}<br>Instructors: {{ course.instructors }}</p>
  </div>
  {% endfor %}
</section>
