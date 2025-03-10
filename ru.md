---
layout: default
title: Тексты
---

# My Documents

{% for page in site.pages %}
  {% if page.path contains 'pages/' %}
    - [{{ page.title | default: page.name }}]({{ page.url }})
  {% endif %}
{% endfor %}
