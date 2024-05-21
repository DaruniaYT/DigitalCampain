---
layout: page
title: Home
id: home
permalink: /
---

![Encabezado](assets/images/encabezado.jpg)

# Bienvenidos a la Wiki de la campaña de Dark Sun

## Enlaces a las páginas

<ul>
  {% for file in site.static_files %}
    {% if file.path contains '/notas/' and file.extname == '.html' %}
      <li><a href="{{ site.baseurl }}{{ file.path }}">{{ file.name | capitalize }}</a></li>
    {% endif %}
  {% endfor %}
</ul>

## Recientemente actualizadas

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
