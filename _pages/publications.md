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
          {{ page.toc_label | default: site.data.ui-text[site.locale].toc_label | default: "On this page" }}
        </h4>
      </header>
      {% include toc.html sanitize=true html=content h_min=2 h_max=3 class="toc__menu" %}
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

  <h2 id="journals">Paper in Peer-Reviewed Journals</h2>
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

  <h2 id="data">Data</h2>
  {% for post in site.publications reversed %}
    {% if post.pubtype == 'data' %}
      {% include archive-single.html %}
    {% endif %}
  {% endfor %}

</section>
