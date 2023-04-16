---
layout: home
---


# Digitale Tools für Cevi-Lager und Kurse

> Wir entwickeln innovative Webtools für Cevi / Pfadi / Jubla, um die Arbeit in der
Abteilung, in Lagern oder Kursen zu vereinfachen.


Auf dieser Seite möchten wir dir eine Übersicht über bereits produktiv einsetzbare Tools und unsere Projekte für zukünftige nützliche Tools bieten.

Die Entwicklung unserer Tools findest du auf [Github](https://github.com/cevi). Gerne darfst du dich an der Entwicklung eines bestehenden Tools beteiligen oder dein eigenes Projekt starten. Kontaktiere uns dazu via Github.

## News:
<ul>
  {% for post in site.posts %}

    {% if post.categories contains 'release' %}
      <li>
        {{ post.date | date: "%d.%m.%Y"}} <a href="{{ post.url }}">{{ post.title }}</a>
      </li>

    {% endif %}
  {% endfor %}
</ul>

## Tools:
{% for post in site.posts %}

  {% if post.categories contains 'tool' %}
    <!-- create a bootstrap grid of album -->
    <div class="col-md-4">
      <div class="card mb-4 box-shadow">
        <img class="card-img-top" src="{{ post.image }}" alt="Card image cap">
        <div class="card-body">
          <h5 class="card-title">{{ post.title }}</h5>
          <p class="card-text">{{ post.excerpt }}</p>
          <div class="d-flex justify-content-between align-items-center">
            <div class="btn-group">
              <a href="{{ post.url }}" class="btn btn-sm btn-outline-secondary">Mehr</a>
            </div>
            <small class="text-muted">{{ post.date | date: "%d.%m.%Y" }}</small>
          </div>
        </div>
      </div>
  {% endif %}
{% endfor %}
