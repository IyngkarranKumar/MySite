---
layout: page
title: Previous work
permalink: /work/
---

Here is a collection of how I've spent my time over the years 

<br><br>

{% for item in site.work %}
  <h3>{{ item.title }}</h3>
  <p>{{ item.description }} - 
  <a href="{{ item.url }}">{{ item.title }}</a></p>
  <br>
{% endfor %}