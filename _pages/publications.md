---
title: "Publications"
layout: archive
permalink: /publications/
author_profile: true
toc: true
---

{% if page.toc %}
  <aside class="sidebar__right sticky">
    <nav class="toc">
      <header>
        <h4 class="nav__title">
          <i class="fas fa-{{ page.toc_icon | default: 'align-justify' }}"></i>
          {{ page.toc_label | default: site.data.ui-text[site.locale].toc_label | default: "On this page" }}
        </h4>
      </header>
      {% include toc.html html=content sanitize=true class="toc__menu" %}
    </nav>
  </aside>
{% endif %}

<h2>Chapter in Edited Books</h2>
{% for post in site.publications reversed %}
  {% if post.pubtype == 'chapter' %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

<h2>Paper in Peer-Reviewed Journals</h2>
{% for post in site.publications reversed %}
  {% if post.pubtype == 'p-r paper' %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

<h2>Conference Papers</h2>
{% for post in site.publications reversed %}
  {% if post.pubtype == 'conf paper' %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

<h2>Data</h2>
{% for post in site.publications reversed %}
  {% if post.pubtype == 'data' %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

{% if author.googlescholar %}
  <p>You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a></u>.</p>
{% endif %}

{% include base_path %}
