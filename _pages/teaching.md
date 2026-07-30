---
layout: page
title: Teaching
permalink: /teaching/
description: Materials for taught courses.
nav: true
#nav_order: 2
#display_categories: work
horizontal: false
---


<!-- pages/teaching.md -->
<div class="projects">

  <!-- 1. GROUP ALL COURSES DYNAMICALLY BY THEIR YEAR VALUE -->
  {%- assign grouped_courses = site.teaching | group_by: "year" -%}
  
  <!-- 2. LOOP THROUGH EACH YEAR GROUP (e.g., 2024-25, 2025, 2026) -->
  {%- for group in grouped_courses -%}
  
    <!-- Dynamic Year Header Element -->
    <h2 class="year-heading" style="margin-top: 2.5rem; margin-bottom: 1.5rem; border-bottom: 2px solid var(--global-divider-color); padding-bottom: 0.5rem; font-weight: bold;">
      {{ group.name }}
    </h2>
    
    <div class="container">
      <!-- Grid layout matching the travel style configuration -->
      <div class="row row-cols-1 row-cols-md-3 g-4">
      
      <!-- 3. LOOP THROUGH ALL INDIVIDUAL COURSES INSIDE THIS SPECIFIC YEAR -->
      {%- assign sorted_courses = group.items | sort: "importance" -%}
      {%- for course in sorted_courses -%}
        <div class="col">
          <!-- Travel Card Visual Shell Layout -->
          <div class="card h-100 shadow-sm border-0" style="border-radius: 6px; overflow: hidden; background: #ffffff; box-shadow: 0 4px 12px rgba(0,0,0,0.08) !important;">
            
            <!-- Card Image Deck -->
            <div class="img-container" style="height: 220px; overflow: hidden;">
              <img src="{{ course.img | relative_url }}" class="card-img-top" style="width: 100%; height: 100%; object-fit: cover;" alt="{{ course.title }}">
            </div>
            
            <!-- Card Metadata Body Deck -->
            <div class="card-body p-4" style="display: flex; flex-direction: column; justify-content: flex-start;">
              <h3 class="card-title font-weight-bold" style="font-size: 1.75rem; margin-bottom: 0.75rem; color: #000000;">
                {{ course.title }}
              </h3>
              <p class="card-text text-muted" style="font-size: 1rem; color: #6c757d; line-height: 1.5; margin-bottom: 0;">
                {{ course.description }} &middot; {{ course.semester }}<br>
                {{ course.year }} &middot; {{ course.institution }}
              </p>
            </div>

          </div>
        </div>
      {%- endfor %}
      
      </div>
    </div>

  {%- endfor %}

</div>



# <!-- pages/teaching.md -->
# <div class="projects">

#     <!-- ================= 2026 COURSES ================= -->
#   <h2 class="year-heading" style="margin-top: 2rem; border-bottom: 2px solid var(--global-divider-color); padding-bottom: 0.5rem;">2026</h2>
#   {%- assign courses_2026 = site.teaching | where: "year", 2026 | sort: "importance" -%}
#   <div class="container">
#     <div class="row row-cols-2">
#     {%- for project in courses_2026 -%}
#       {% include projects_horizontal.html %}
#     {%- endfor %}
#     </div>
#   </div>

#    <!-- ================= 2025 COURSES ================= -->
#   <h2 class="year-heading" style="margin-top: 3rem; border-bottom: 2px solid var(--global-divider-color); padding-bottom: 0.5rem;">2025</h2>
#   {%- assign courses_2025 = site.teaching | where: "year", 2025 | sort: "importance" -%}
#   <div class="container">
#     <div class="row row-cols-2">
#     {%- for project in courses_2025 -%}
#       {% include projects_horizontal.html %}
#     {%- endfor %}
#     </div>
#   </div>

#    <!-- ================= 2024 COURSES ================= -->
#   <h2 class="year-heading" style="margin-top: 2rem; border-bottom: 2px solid var(--global-divider-color); padding-bottom: 0.5rem;">2024</h2>
#   {%- assign courses_2024 = site.teaching | where: "year", 2024 | sort: "importance" -%}
#   <div class="container">
#     <div class="row row-cols-2">
#     {%- for project in courses_2024 -%}
#       {% include projects_horizontal.html %}
#     {%- endfor %}
#     </div>
#   </div>

#    <!-- ================= 2023 COURSES ================= -->
#   <h2 class="year-heading" style="margin-top: 2rem; border-bottom: 2px solid var(--global-divider-color); padding-bottom: 0.5rem;">2023</h2>
#   {%- assign courses_2023 = site.teaching | where: "year", 2023 | sort: "importance" -%}
#   <div class="container">
#     <div class="row row-cols-2">
#     {%- for project in courses_2023 -%}
#       {% include projects_horizontal.html %}
#     {%- endfor %}
#     </div>
#   </div>

#    <!-- ================= 2022 COURSES ================= -->
#   <h2 class="year-heading" style="margin-top: 2rem; border-bottom: 2px solid var(--global-divider-color); padding-bottom: 0.5rem;">2022</h2>
#   {%- assign courses_2022 = site.teaching | where: "year", 2022 | sort: "importance" -%}
#   <div class="container">
#     <div class="row row-cols-2">
#     {%- for project in courses_2022 -%}
#       {% include projects_horizontal.html %}
#     {%- endfor %}
#     </div>
#   </div>

#   <!-- ================= 2021 COURSES ================= -->
#   <h2 class="year-heading" style="margin-top: 2rem; border-bottom: 2px solid var(--global-divider-color); padding-bottom: 0.5rem;">2021</h2>
#   {%- assign courses_2021 = site.teaching | where: "year", 2021 | sort: "importance" -%}
#   <div class="container">
#     <div class="row row-cols-2">
#     {%- for project in courses_2021 -%}
#       {% include projects_horizontal.html %}
#     {%- endfor %}
#     </div>
#   </div>

#    <!-- ================= 2020 COURSES ================= -->
#   <h2 class="year-heading" style="margin-top: 2rem; border-bottom: 2px solid var(--global-divider-color); padding-bottom: 0.5rem;">2020</h2>
#   {%- assign courses_2020 = site.teaching | where: "year", 2020 | sort: "importance" -%}
#   <div class="container">
#     <div class="row row-cols-2">
#     {%- for project in courses_2020 -%}
#       {% include projects_horizontal.html %}
#     {%- endfor %}
#     </div>
#   </div>

#   <!-- ================= 2019 COURSES ================= -->
#   <h2 class="year-heading" style="margin-top: 2rem; border-bottom: 2px solid var(--global-divider-color); padding-bottom: 0.5rem;">2019</h2>
#   {%- assign courses_2019 = site.teaching | where: "year", 2019 | sort: "importance" -%}
#   <div class="container">
#     <div class="row row-cols-2">
#     {%- for project in courses_2019 -%}
#       {% include projects_horizontal.html %}
#     {%- endfor %}
#     </div>
#   </div>

# </div>

