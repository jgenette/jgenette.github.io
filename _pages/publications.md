---
title: "Publications"
layout: archive
permalink: /publications/
author_profile: true
toc: true
---

<section class="page__content" itemprop="text">

  <!-- TOC Sidebar -->
  {% if page.toc %}
<aside class="sidebar__right">
  <nav class="toc">
    <header>
      <h4 class="nav__title">
        <i class="fas fa-align-justify"></i>
        On This Page
      </h4>
    </header>
    <ul class="toc__menu">
<ul class="toc__menu">
  <li><a href="#chapters">Chapter in Edited Books</a></li>
  <li><a href="#journals">Journal Papers</a></li>
  <li><a href="#conferences">Conference Papers</a></li>
  <li><a href="#software">Software</a></li>
  <li><a href="#data">Data</a></li>
  <li><a href="#thesis">Thesis</a></li>
</ul>
    </ul>
  </nav>
</aside>
  {% endif %}

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
