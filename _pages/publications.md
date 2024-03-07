---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

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

