---
layout: page
title: Home
id: home
permalink: /
---

# Bienvenidos a la Wiki de la campaña de Dark Sun

## Acceso rápido a las páginas

<ul>
  <li><a href="{{ site.baseurl }}/notas/Athas.html">Athas</a></li>
  <li><a href="{{ site.baseurl }}/notas/LIBERTAD.html">LIBERTAD</a></li>
  <li><a href="{{ site.baseurl }}/notas/Rey Hechicero.html">Rey Hechicero</a></li>
  <!-- Añade más enlaces según sea necesario -->
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
