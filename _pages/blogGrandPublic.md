---
layout: default
title: Blog Tect
permalink: /blog-grand-public/
---

{% for post in site.categories.grand-public %}
  <p><a href="{{ post.url }}">{{ post.title }}</a><br>
  {{ post.description }}<br>
  
  📅 {{ post.date | date: "%-d" }}
{% assign m = post.date | date: "%-m" %}
{% case m %}
  {% when '1' %}janvier
  {% when '2' %}février
  {% when '3' %}mars
  {% when '4' %}avril
  {% when '5' %}mai
  {% when '6' %}juin
  {% when '7' %}juillet
  {% when '8' %}août
  {% when '9' %}septembre
  {% when '10' %}octobre
  {% when '11' %}novembre
  {% when '12' %}décembre
{% endcase %}
{{ post.date | date: "%Y" }}
  
{% endfor %}
