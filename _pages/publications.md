---
title: "Publications"
layout: archive
permalink: /publications/
author_profile: true
toc: true
---

<section class="page__content" itemprop="text">

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

</section>

