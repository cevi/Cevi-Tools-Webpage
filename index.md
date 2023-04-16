---
layout: home
---


# Digitale Tools für Cevi-Lager und Kurse

> Wir entwickeln innovative Webtools für Cevi / Pfadi / Jubla, um die Arbeit in der
Abteilung, in Lagern oder Kursen zu vereinfachen.


Auf dieser Seite möchten wir dir eine Übersicht über bereits produktiv einsetzbare Tools und unsere Projekte für zukünftige nützliche Tools bieten.

Die Entwicklung unserer Tools findest du auf [Github](https://github.com/cevi). Gerne darfst du dich an der Entwicklung eines bestehenden Tools beteiligen oder dein eigenes Projekt starten. Kontaktiere uns dazu via Github.

## News
<ul>
  {% for post in site.posts %}

    {% if post.categories contains 'release' %}
      <li>
        {{ post.date | date: "%d.%m.%Y"}} <a href="{{ post.url }}">{{ post.title }}</a>
      </li>

    {% endif %}
  {% endfor %}
</ul>

## Tools
<!-- create a flexbox grid (3 columns) with all posts from the category "tools", and create bootstrap-card like cards in pure html. -->
<div id="tools">
<div class="row">
{% for post in site.posts %}
  {% if post.categories contains 'tool' %}
<div class="column">
<a href="{{ post.url }}">
  <div class="card">
    <div class="card-body">
      <div class="img-holder"><img src="{{ post.image }}" alt="{{ post.title }}"></div>
      <div class="text-holder">
        {% if post.categories contains 'tool-ready-to-use' %}
          <span class="badge badge-ready-to-use">Bereit zum Einsatz</span>
        {% endif %}
        {% if post.categories contains 'tool-in-development' %}
          <span class="badge badge-in-development">In Entwicklung</span>
        {% endif %}
        {% if post.categories contains 'tool-diy' %}
          <span class="badge badge-diy">Selber erstellen</span>
        {% endif %}

        <h3 class="card-title">{{ post.title }}</h3>
      
        <p class="card-text">{{ post.excerpt }}</p>

        {% if post.deplyoment %}
          <a class="deployment" href="{{ post.deplyoment }}">
            <img class="svg-icon" src="{{ '/assets/link-solid.svg' | relative_url }}"></img> {{ post.deplyoment }}
          </a>
        {% endif %}
      </div>
    </div>
  </div>
</a>
</div>
  {% endif %}
{% endfor %}
</div>
</div>