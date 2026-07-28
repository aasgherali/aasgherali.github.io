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

  <!-- ================= 2019 COURSES ================= -->
  <h2 class="year-heading" style="margin-top: 2rem; border-bottom: 2px solid var(--global-divider-color); padding-bottom: 0.5rem;">2019</h2>
  {%- assign courses_2019 = site.teaching | where: "year", 2019 | sort: "importance" -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in courses_2019 -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>

    <!-- ================= 2020 COURSES ================= -->
  <h2 class="year-heading" style="margin-top: 2rem; border-bottom: 2px solid var(--global-divider-color); padding-bottom: 0.5rem;">2020</h2>
  {%- assign courses_2020 = site.teaching | where: "year", 2020 | sort: "importance" -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in courses_2020 -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>

    <!-- ================= 2021 COURSES ================= -->
  <h2 class="year-heading" style="margin-top: 2rem; border-bottom: 2px solid var(--global-divider-color); padding-bottom: 0.5rem;">2021</h2>
  {%- assign courses_2021 = site.teaching | where: "year", 2021 | sort: "importance" -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in courses_2021 -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>

    <!-- ================= 2022 COURSES ================= -->
  <h2 class="year-heading" style="margin-top: 2rem; border-bottom: 2px solid var(--global-divider-color); padding-bottom: 0.5rem;">2022</h2>
  {%- assign courses_2022 = site.teaching | where: "year", 2022 | sort: "importance" -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in courses_2022 -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>

    <!-- ================= 2023 COURSES ================= -->
  <h2 class="year-heading" style="margin-top: 2rem; border-bottom: 2px solid var(--global-divider-color); padding-bottom: 0.5rem;">2023</h2>
  {%- assign courses_2023 = site.teaching | where: "year", 2023 | sort: "importance" -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in courses_2023 -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>

    <!-- ================= 2024 COURSES ================= -->
  <h2 class="year-heading" style="margin-top: 2rem; border-bottom: 2px solid var(--global-divider-color); padding-bottom: 0.5rem;">2024</h2>
  {%- assign courses_2024 = site.teaching | where: "year", 2024 | sort: "importance" -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in courses_2024 -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>


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

