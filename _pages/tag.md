---
layout: default
title: Tags
permalink: /tags/
---

{% assign sortedTags = site.tags | sort %}
{% for tag in sortedTags %}

<a href="#{{tag[0]}}">{{ tag[0] | replace: "-", "&nbsp;" }}&nbsp;({{ tag[1] | size }})</a>

{% endfor %}
