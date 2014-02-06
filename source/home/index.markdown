---
layout: page
title: "home"
date: 2014-02-05 21:35
comments: true
sharing: true
footer: true
---


<aside class="sidebar">
  {% if site.blog_index_asides.size %}
    {% include_array blog_index_asides %}
  {% else %}
    {% include_array default_asides %}
  {% endif %}
</aside>