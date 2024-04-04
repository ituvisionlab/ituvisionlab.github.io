---
layout: page
permalink: /publications/
title: publications
description: publications by categories in reversed chronological order.
years: [2024, 2023, 2022, 2021] # TO UPDATE FOR NEW PAPERS
nav: true
nav_order: 2
---

<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>