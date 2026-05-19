---
layout: page
title: ePortfolio
page_heading: Projects in Courses
permalink: /eportfolio/
---

{% assign lectures_sorted = site.lectures | sort: "semester_order" | reverse %}
{% assign semesters = lectures_sorted | map: "semester" | uniq %}

{% for sem in semesters %}

<div class="semester-divider">

  <span>{{ sem }}</span>

</div>

<div class="lecture-grid">

{% for lecture in lectures_sorted %}

  {% if lecture.semester == sem %}

    <a href="{{ lecture.url }}" class="lecture-card">

      <img src="{{ lecture.image }}" alt="{{ lecture.title }}">

      <div class="lecture-content">

        <h2>{{ lecture.title }}</h2>

        <p>{{ lecture.excerpt }}</p>

        <div class="lecture-course">
          {{ lecture.course }}
        </div>

      </div>

    </a>

  {% endif %}

{% endfor %}

</div>

{% endfor %}
