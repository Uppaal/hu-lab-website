---
layout: page
title: "News"
subtitle: "Lab updates"
---

<ul>
{% for n in site.data.news %}
  <li><span class="text-muted">{{ n.date }}:</span> {{ n.text }}</li>
{% endfor %}
</ul>
