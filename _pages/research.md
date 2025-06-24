---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
header:
  og_image: "research/ecdf.png"
---

Currently, I am working on the acoustic characteristics of babbles and early word production in the speech of typically developing children and children with hearing impairment. My research approach is mainly quantitative and inspired by laboratory phonology. Besides the phonetics of child speech, I am also working on methodological questions related to speech sciences and on (Italian) dialectology.



<nbsp>

{% include base_path %}

{% assign ordered_pages = site.research | sort:"order_number" %}

{% for post in ordered_pages %}
  {% include archive-single.html type="grid" %}
{% endfor %})

