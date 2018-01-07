---
layout: default
title: Upcoming Training Events
excerpt: In-person and online upcoming conferences and training.
---

Upcoming Training and Conference Events
=======================================

<div class="list-group">
  {% for event in site.data.training-events %}
    {% assign eventSeconds = (event.endDate | date: "%s" | plus: 0) %}
    {% assign nowSeconds = (site.time | date: "%s" | plus: 0 %}
    {% if eventSeconds == 0 or eventSeconds > nowSeconds %}     
      {% include training-event-list-item.html event=event %}
    {% endif %}
  {% endfor %}
</div>