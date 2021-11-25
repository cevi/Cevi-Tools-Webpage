---
layout: home
---

# Digitale Tools für Cevi-Lager und Kurse

Unsere Tools findet man auf [Github](https://github.com/cevi).

## News: 
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>