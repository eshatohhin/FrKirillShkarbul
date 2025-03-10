---
layout: default
title: Тексты
---

# Тексты

{% for page in site.pages %}
  {% if page.path contains 'ru/' %}
    - [{{ page.title | default: page.name }}]({{ page.url }})
  {% endif %}
{% endfor %}
