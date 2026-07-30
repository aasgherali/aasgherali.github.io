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

---
layout: page
title: teaching
permalink: /teaching/
description: Materials for taught courses.
nav: true
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
