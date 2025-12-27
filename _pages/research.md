---
layout: archive
title: Research
permalink: /research/
author_profile: true
header:
  og_image: research/ecdf.png
---

Currently, I am working on the acoustic characteristics of babbles and early word production in the speech of typically developing children and children with hearing impairment. My research approach is mainly quantitative and inspired by laboratory phonology. Besides the phonetics of child speech, I am also working on methodological questions related to speech sciences and on (Italian) dialectology.


{% assign projects = site.research | sort: "order_number" %}

## Child Speech & Development
<div class="research-grid">
{% for post in projects %}
  {% if post.themes contains "child_speech" %}
    {% include research-card.html post=post %}
  {% endif %}
{% endfor %}
</div>

## Hearing Impairment
<div class="research-grid">
{% for post in projects %}
  {% if post.themes contains "hearing_impairment" %}
    {% include research-card.html post=post %}
  {% endif %}
{% endfor %}
</div>

## Laboratory Phonology
<div class="research-grid">
{% for post in projects %}
  {% if post.themes contains "laboratory_phonology" %}
    {% include research-card.html post=post %}
  {% endif %}
{% endfor %}
</div>

## Methods & Speech Sciences
<div class="research-grid">
{% for post in projects %}
  {% if post.themes contains "methods" %}
    {% include research-card.html post=post %}
  {% endif %}
{% endfor %}
</div>

## Dialectology
<div class="research-grid">
{% for post in projects %}
  {% if post.themes contains "dialectology" %}
    {% include research-card.html post=post %}
  {% endif %}
{% endfor %}
</div>
