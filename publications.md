---
layout: page
title: "Publications"
subtitle: "Selected and recent papers"
---

{% for block in site.data.publications %}
### {{ block.year }}

{% if block.items and block.items.size > 0 %}
<ol>
{% for it in block.items %}
  <li class="mb-2">
    <div class="fw-semibold">{{ it.title }}</div>
    <div class="text-muted">{{ it.authors }}</div>
    <div>{{ it.venue }}</div>
    {% if it.links %}
      <div class="mt-1">
        {% for l in it.links %}
          <a class="badge-lite text-decoration-none" href="{{ l.url }}">{{ l.label }}</a>
        {% endfor %}
      </div>
    {% endif %}
  </li>
{% endfor %}
</ol>
{% else %}
<p class="text-muted">No entries yet.</p>
{% endif %}

{% endfor %}
