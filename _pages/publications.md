---
title: "Publications"
layout: archive
permalink: /publications/
author_profile: true
toc: true
---

{% if page.toc %}
<div class="sidebar sticky" style="width: 15.2542372881%; float: right !important; margin-left: 1.6949152542% !important; opacity: 1;">
  <nav class="toc">
    <header>
      <h2 class="nav__title">
        <i class="fas fa-{{ page.toc_icon | default: 'align-justify' }}"></i> 
        {{ page.toc_label | default: site.data.ui-text[site.locale].toc_label | default: "On this page" }}
      </h2>
    </header>
    {% include toc.html sanitize=true html=content h_min=1 h_max=6 class="toc__menu" %}
  </nav>
</div>
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
