---
layout: page
title: Previous work
---

Here's some of the work I've done/am doing.

<br><br>

{% for item in site.work %}
  <h3>{{ item.title }}</h3>
  <p>{{ item.description }} - 
  <a href="{{ item.url }}">{{ item.title }}</a></p>
  <br>
{% endfor %}