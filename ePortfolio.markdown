---
layout: page
title: ePortfolio
page_heading: Projects in Courses
permalink: /eportfolio/
---
{% assign semesters = site.lectures | map: "semester" | uniq %}

{% for sem in semesters %}

<div class="semester-divider">

  <span>{{ sem }}</span>

</div>

<div class="lecture-grid">

  {% for lecture in site.lectures %}

    {% if lecture.semester == sem %}

      <a href="{{ lecture.url }}" class="lecture-card">

        <img src="{{ lecture.image }}" alt="{{ lecture.title }}">

        <div class="lecture-content">

          <h2>{{ lecture.title }}</h2>

          <p>{{ lecture.excerpt }}</p>

        </div>

      </a>

    {% endif %}

  {% endfor %}

</div>

{% endfor %}
