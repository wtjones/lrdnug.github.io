---
layout: default
title: Upcoming Training Events
excerpt: In-person and online upcoming conferences and training.
---

Upcoming Training and Conference Events
========================

<div class="list-group">
  {% for event in site.data.training-events %}
  {% include training-event-list-item.html event=event %}
  {% endfor %}
</div>