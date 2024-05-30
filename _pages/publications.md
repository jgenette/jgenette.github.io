---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

<aside class="sidebar__right">
<nav class="toc" markdown="1">
<header><h4 class="nav__title"><i class="fas fa-{{ include.icon | default: 'file-alt' }}"></i> {{ include.title | default: site.data.ui-text[site.locale].toc_label }}</h4></header>
*  Auto generated table of contents
{:toc .toc__menu}
</nav>
</aside>

<h2>Chapter in edited books</h2>
{% for post in site.publications reversed %}
  {% if post.pubtype == 'chapter' %}
      {% include archive-single.html %}
  {% endif %}
{% endfor %}

<h2>Paper in peer-reviewed journal</h2>
{% for post in site.publications reversed %}
  {% if post.pubtype == 'p-r paper' %}
      {% include archive-single.html %}
  {% endif %}
{% endfor %}

<h2>Conference papers</h2>
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
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

