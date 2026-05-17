---
layout: page
title: ePortfolio
page_heading: Lectures
permalink: /eportfolio/
---
<div class="lecture-grid">

{% for lecture in site.lectures %}

<a href="{{ lecture.url }}" class="lecture-card">

  <img src="{{ lecture.image }}" alt="{{ lecture.title }}">

  <div class="lecture-content">

    <h2>{{ lecture.title }}</h2>

    <p>{{ lecture.excerpt }}</p>

  </div>

</a>

{% endfor %}

</div>
