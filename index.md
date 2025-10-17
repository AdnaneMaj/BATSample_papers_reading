---
layout: default
title: Upcoming
---

<h1>Upcoming Presentations</h1>
<p><a class="btn" href="https://github.com/AdnaneMaj/BATSample_papers_reading/issues/new?template=presentation.yml">Submit your paper</a></p>

<ul>
{% assign today = 'now' | date: '%Y-%m-%d' %}
{% assign upcoming = site.presentations | where_exp: "p", "p.date >= today" | sort: "date" %}
{% for p in upcoming %}
  <li>
    <a href="{{ p.url }}">{{ p.title }}</a> — {{ p.date }} — 
    <a href="/presenters/{{ p.presenter_username }}.html">{{ p.presenter_first }} {{ p.presenter_last }}</a>
  </li>
{% endfor %}
</ul>
