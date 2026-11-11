---
title: About
heading: Welcome.
permalink: /
description: Mohammad Naderitabar, PhD candidate in Economics at IIES, Stockholm University. Macroeconomics, industrial organization, innovation, and information economics.
---

<div class="biography" markdown="1">
I am a PhD candidate in Economics at the [Institute for International Economic Studies (IIES)]({{ site.affiliation.institute_url }}), [Stockholm University]({{ site.affiliation.university_url }}).

My research interests include **macroeconomics, industrial organization, innovation, and information economics**. My current work studies how market structure, innovation incentives, and household behavior shape economic growth and inequality.
</div>

<section class="content-section" aria-labelledby="research-heading">
  <div class="section-heading">
    <h2 id="research-heading">Research</h2>
    <a class="section-link" href="{{ '/research/' | relative_url }}">All research <span aria-hidden="true">→</span></a>
  </div>
  {% for paper in site.data.research.papers limit: 1 %}
    {% include research-paper.html paper=paper %}
  {% endfor %}
</section>

<section class="content-section contact-section" aria-labelledby="contact-heading">
  <h2 id="contact-heading">Get in touch</h2>
  <p>I am based at IIES, Stockholm University. You can reach me at <a href="mailto:{{ site.author.email }}">{{ site.author.email }}</a>.</p>
</section>
