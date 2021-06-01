---
layout: default
title: Tags
permalink: /tags/
---

{% assign sortedTags = site.tags | sort %}
{% for tag in sortedTags %}

  <a href="#{{tag[0]}}">{{ tag[0] | replace: "-", "&nbsp;" }}&nbsp;({{ tag[1] | size }})</a>

{% endfor %}

{% for tag in sortedTags %}

  <h2 id="{{ tag[0] }}">{{ tag[0] | replace: "-", "&nbsp;" }}</h2>
  
  {% for post in tag[0] %}
    <a href="{{ post.url }}" title="{{ post.title }}">{{post.title}}</a>
  {% endfor %}

{% endfor %}
