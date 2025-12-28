---
layout: archive
title: Research
permalink: /research/
author_profile: true
header:
  og_image: research/ecdf.png
---
<!-- ===================== -->
<!-- Research page intro  -->
<!-- ===================== -->

<div class="research-intro">
  <p>
    My research focuses on the acoustic and phonetic properties of child speech,
    with particular attention to hearing impairment, laboratory phonology,
    and methodological issues in speech sciences.
  </p>
</div>

<hr>

<!-- ===================== -->
<!-- Filter UI            -->
<!-- ===================== -->

<div class="research-filter">
  <label for="project-filter"><strong>Filter by topic:</strong></label>
  <select id="project-filter">
    <option value="all">All projects</option>
    <option value="acoustics">Acoustics</option>
    <option value="phonetics">Phonetics</option>
    <option value="babbling">Babbling</option>
    <option value="child speech">Child speech</option>
    <option value="hearing impairment">Hearing impairment</option>
    <option value="methods">Methods</option>
    <option value="dialectology">Dialectology</option>
  </select>

  <p id="filter-status" style="font-size:0.85rem;color:#555;"></p>
</div>

<hr>

<!-- ===================== -->
<!-- Research cards       -->
<!-- ===================== -->

<div id="research-cards" class="research-grid">

  <!-- CARD 1 -->
  <div class="research-card"
       data-tags="acoustics babbling child speech hearing impairment">

    <h3>
      <a href="/research/early-babbling/">
        Acoustic properties of early babbling
      </a>
    </h3>

    <p>
      Quantitative analysis of spectral and temporal characteristics of babbling
      in typically developing children and children with hearing impairment.
    </p>

    <p class="research-tags">
      <span class="research-tag">acoustics</span>
      <span class="research-tag">babbling</span>
      <span class="research-tag">child speech</span>
      <span class="research-tag">hearing impairment</span>
    </p>
  </div>

  <!-- CARD 2 -->
  <div class="research-card"
       data-tags="phonetics methods laboratory phonology">

    <h3>
      <a href="/research/phonetic-methods/">
        Methodological issues in child speech phonetics
      </a>
    </h3>

    <p>
      Investigation of methodological choices in acoustic and articulatory
      analyses within a laboratory phonology framework.
    </p>

    <p class="research-tags">
      <span class="research-tag">phonetics</span>
      <span class="research-tag">methods</span>
      <span class="research-tag">laboratory phonology</span>
    </p>
  </div>

  <!-- CARD 3 -->
  <div class="research-card"
       data-tags="dialectology phonetics italian dialects">

    <h3>
      <a href="/research/italian-dialectology/">
        Phonetic variation in Italian dialects
      </a>
    </h3>

    <p>
      Phonetic and acoustic documentation of regional variation in contemporary
      Italian dialects, with attention to segmental and prosodic features.
    </p>

    <p class="research-tags">
      <span class="research-tag">dialectology</span>
      <span class="research-tag">phonetics</span>
      <span class="research-tag">Italian dialects</span>
    </p>
  </div>

</div>

<!-- ===================== -->
<!-- Filtering logic      -->
<!-- ===================== -->

<script>
document.addEventListener("DOMContentLoaded", function () {
  const filter = document.getElementById("project-filter");
  const cards = document.querySelectorAll(".research-card");
  const status = document.getElementById("filter-status");

  filter.addEventListener("change", function () {
    const value = this.value;

    cards.forEach(function (card) {
      const tags = card.getAttribute("data-tags") || "";

      if (value === "all" || tags.includes(value)) {
        card.style.display = "";
      } else {
        card.style.display = "none";
      }
    });

    status.textContent =
      value === "all"
        ? ""
        : "Showing projects tagged with: “" + value + "”.";
  });
});
</script>
