---
layout: page
title: Home
id: home
permalink: /
---

![Encabezado](assets/encabezado.jpg)

# Wiki de la campaña de Dark Sun

## Enlaces a las páginas

<ul>
  {% for file in site.static_files %}
    {% if file.path contains '/notas/' and file.extname == '.html' %}
      <li><a href="{{ site.baseurl }}{{ file.path }}">{{ file.name | capitalize }}</a></li>
    {% endif %}
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
