---
layout: default
title: Тексты
---

<!-- <audio controls>
  <source src="es/audio/001.opus" type="audio/mpeg">
  Your browser does not support the audio element.
</audio> -->

# Тексты с канала [@иерейКириллШкарбуль](https://www.youtube.com/@%D0%B8%D0%B5%D1%80%D0%B5%D0%B9%D0%9A%D0%B8%D1%80%D0%B8%D0%BB%D0%BB%D0%A8%D0%BA%D0%B0%D1%80%D0%B1%D1%83%D0%BB%D1%8C)

<ul>
{% assign sorted_pages = site.pages | reverse %}
{% for page in sorted_pages %}
  {% if page.path contains 'ru/' %}
    {% assign filename = page.path | split: '/' | last %}
    {% assign filename = filename | replace: '.md', '' %}
    {% assign github_edit_url = "https://github.com/eshatohhin/FrKirillShkarbul/edit/master/" | append: page.path %}
    <li>
      <a href="{{ page.url | relative_url }}">[{{ filename | default: page.name }}] {{page.title}}</a>
      <a href="{{ github_edit_url }}" target="_blank" style="margin-left:10px; color: red;">✏️</a>
    </li>
  {% endif %}
{% endfor %}
</ul>

# Тексты с канала [@frkirillshkarbul5107](https://www.youtube.com/@frkirillshkarbul5107)

<ul>
{% assign sorted_pages = site.pages | reverse %}
{% for page in sorted_pages %}
  {% if page.path contains 'en/' %}
    {% assign filename = page.path | split: '/' | last %}
    {% assign filename = filename | replace: '.md', '' %}
    {% assign github_edit_url = "https://github.com/eshatohhin/FrKirillShkarbul/edit/master/" | append: page.path %}
    <li>
      <a href="{{ page.url | relative_url }}">[{{ filename | default: page.name }}] {{page.title}}</a>
      <a href="{{ github_edit_url }}" target="_blank" style="margin-left:10px; color: red;">✏️</a>
      {% for page in sorted_pages %}
        {% if page.path contains 'es/' and page.path contains filename %}
          {% assign github_edit_url = "https://github.com/eshatohhin/FrKirillShkarbul/edit/master/" | append: page.path %}
          <ul>
            Spanish: 
            <a href="{{ page.url | relative_url }}">{{page.title}}</a>
            <a href="{{ github_edit_url }}" target="_blank" style="margin-left:10px; color: red;">✏️</a>
          </ul>
        {% endif %}
      {% endfor %}
      {% for page in sorted_pages %}
        {% if page.path contains 'fr/' and page.path contains filename %}
          {% assign github_edit_url = "https://github.com/eshatohhin/FrKirillShkarbul/edit/master/" | append: page.path %}
          <ul>
            French: 
            <a href="{{ page.url | relative_url }}">{{page.title}}</a>
            <a href="{{ github_edit_url }}" target="_blank" style="margin-left:10px; color: red;">✏️</a>
          </ul>
        {% endif %}
      {% endfor %}
    </li>
  {% endif %}
{% endfor %}
</ul>


