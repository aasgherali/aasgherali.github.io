---
layout: page
title: Teaching
permalink: /teaching/
description: Materials for taught courses.
nav: true
#nav_order: 2
#display_categories: work
horizontal: true
---

<!-- pages/teaching.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized teaching materials -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_teaching = site.teaching | where: "category", category -%}
  {%- assign sorted_teaching = categorized_teaching | sort: "importance" %}
  <!-- Generate cards for each course -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_teaching -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_teaching -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}

{%- else -%}
<!-- Display teaching materials without categories -->
  {%- assign sorted_teaching = site.teaching | sort: "importance" -%}
  <!-- Generate cards for each course -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_teaching -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_teaching -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div>


<!-- pages/teaching.md -->
<div class="projects">

  <!-- ================= 2026 COURSES ================= -->
  <h2 class="year-heading" style="margin-top: 2rem; border-bottom: 2px solid var(--global-divider-color); padding-bottom: 0.5rem;">2026</h2>
  {%- assign courses_2026 = site.teaching | where: "year", 2026 | sort: "importance" -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in courses_2026 -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>

  <!-- ================= 2025 COURSES ================= -->
  <h2 class="year-heading" style="margin-top: 3rem; border-bottom: 2px solid var(--global-divider-color); padding-bottom: 0.5rem;">2025</h2>
  {%- assign courses_2025 = site.teaching | where: "year", 2025 | sort: "importance" -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in courses_2025 -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>

</div>

