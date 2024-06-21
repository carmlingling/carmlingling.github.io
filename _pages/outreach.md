---
layout: page
title: outreach and EDI
permalink: /outreach/
description:
nav: true
---

When she is not exploring the transport of droplets, or thinking about why sand is so weird, Carmen is making science accessible to a wider audience, by participating in several science communication initiatives worldwide. This experience has enabled her to share her passion about science with the public, with a focus on children, the next generation of scientists.  Intertwined with her teaching and outreach are the threads of equity and inclusion. Recognizing the power of representation,Carmen has advocated for diverse voices and role models in STEM through my work in Promoting Inclusion in Physics and Astronomy. This group challenges the stereotype of 'who is a physicist' and through creating a community-led and focused network at McMaster University. Below you can learn more about the initiatives she is involved in. In case you are interested in collaborating on a science communication project, feel free to [contact](mailto:{{site.email}}).

# "<!-- pages/projects.md -->
<div class="projects">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_projects = site.projects | where: "category", category %}
  {% assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display projects without categories -->

{% assign sorted_projects = site.projects | sort: "importance" %}

  <!-- Generate cards for each project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>

"
