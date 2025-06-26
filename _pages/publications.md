---
title: "Publications"
layout: archive
permalink: /publications/
author_profile: true
toc: true
---


  <!-- Main Content -->
  <h2 id="chapters">Chapter in Edited Books</h2>
  {% for post in site.publications reversed %}
    {% if post.pubtype == 'chapter' %}
      {% include archive-single.html %}
    {% endif %}
  {% endfor %}

  <h2 id="journals">Journal Papers</h2>
  {% for post in site.publications reversed %}
    {% if post.pubtype == 'p-r paper' %}
      {% include archive-single.html %}
    {% endif %}
  {% endfor %}

  <h2 id="conferences">Conference Papers</h2>
  {% for post in site.publications reversed %}
    {% if post.pubtype == 'conf paper' %}
      {% include archive-single.html %}
    {% endif %}
  {% endfor %}

  <h2 id="data">Software</h2>
  {% for post in site.publications reversed %}
    {% if post.pubtype == 'software' %}
      {% include archive-single.html %}
    {% endif %}
  {% endfor %}

<h2 id="data">Data</h2>
  {% for post in site.publications reversed %}
    {% if post.pubtype == 'data' %}
      {% include archive-single.html %}
    {% endif %}
  {% endfor %}

  <h2 id="thesis">Theses</h2>
  {% for post in site.publications reversed %}
    {% if post.pubtype == 'thesis' %}
      {% include archive-single.html %}
    {% endif %}
  {% endfor %}

  
</section>
