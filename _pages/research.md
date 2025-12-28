---
layout: archive
title: Research
permalink: /research/
author_profile: true
header:
  og_image: research/ecdf.png
---

<!-- ===================== -->
<!-- Inline styles        -->
<!-- ===================== -->

<style>
.research-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 1.5rem;
}

.research-card {
  background-color: #f5f5f5;
  border: 1px solid #e0e0e0;
  padding: 1rem;
}

.research-card-image {
  margin-bottom: 0.75rem;
}

.research-card-image img {
  width: 100%;
  height: auto;
}

.research-card h3 {
  margin-top: 0;
  margin-bottom: 0.25rem;
}

.research-dates {
  font-size: 0.85rem;
  color: #666;
  margin-bottom: 0.5rem;
}

.research-tags {
  font-size: 0.75rem;
  margin: 0.5rem 0;
}

.research-tag {
  display: inline-block;
  border: 1px solid #bbb;
  padding: 0.1rem 0.4rem;
  margin: 0 0.3rem 0.3rem 0;
  background: #fafafa;
}

.research-meta {
  font-size: 0.85rem;
  color: #444;
  margin: 0.25rem 0;
}

.research-filter {
  margin-bottom: 1.5rem;
}
</style>

<!-- ===================== -->
<!-- Research intro       -->
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

  <!-- ===================== -->
  <!-- PROJECT CARD         -->
  <!-- ===================== -->

  <div class="research-card"
       data-tags="acoustics babbling child speech hearing impairment">

    <div class="research-card-image">
      <img src="/assets/images/research/babbling.jpg"
           alt="Spectrogram of early babbling">
    </div>

    <h3>
      <a href="/research/early-babbling/">
        Acoustic properties of early babbling
      </a>
    </h3>

    <p class="research-dates">
      📅 2024–present
    </p>

    <p>
      Quantitative analysis of spectral and temporal characteristics of
      canonical and non-canonical babbling in typically developing children
      and children with hearing impairment.
    </p>

    <p class="research-tags">
      🏷️
      <span class="research-tag">acoustics</span>
      <span class="research-tag">babbling</span>
      <span class="research-tag">child speech</span>
      <span class="research-tag">hearing impairment</span>
    </p>

    <p class="research-meta">
      👥 <strong>Collaborators:</strong> Maria Rossi (University of Milan), John Smith (Oxford)
    </p>

    <p class="research-meta">
      💰 <strong>Funding:</strong> Italian Ministry of Education (PRIN 2022)
    </p>

    <p class="research-meta">
      📚 <strong>Published in:</strong> <em>Journal of Phonetics</em> (2024)
    </p>

  </div>

  <!-- ===================== -->
  <!-- PROJECT CARD         -->
  <!-- ===================== -->

  <div class="research-card"
       data-tags="phonetics methods laboratory phonology">

    <div class="research-card-image">
      <img src="/assets/images/research/methods.jpg"
           alt="Acoustic analysis workflow">
    </div>

    <h3>
      <a href="/research/phonetic-methods/">
        Methodological issues in child speech phonetics
      </a>
    </h3>

    <p class="research-dates">
      📅 2021–2023
    </p>

    <p>
      Examination of methodological choices in acoustic analysis,
      annotation reliability, and reproducibility within a laboratory
      phonology framework.
    </p>

    <p class="research-tags">
      🏷️
      <span class="research-tag">phonetics</span>
      <span class="research-tag">methods</span>
      <span class="research-tag">laboratory phonology</span>
    </p>

    <p class="research-meta">
      👥 <strong>Collaborators:</strong> —
    </p>

    <p class="research-meta">
      💰 <strong>Funding:</strong> —
    </p>

    <p class="research-meta">
      🎤 <strong>Presented at:</strong> LabPhon 18 (2022)
    </p>

  </div>

  <!-- ===================== -->
  <!-- PROJECT CARD         -->
  <!-- ===================== -->

  <div class="research-card"
       data-tags="dialectology phonetics italian dialects">

    <div class="research-card-image">
      <img src="/assets/images/research/dialectology.jpg"
           alt="Italian dialect map">
    </div>

    <h3>
      <a href="/research/italian-dialectology/">
        Phonetic variation in Italian dialects
      </a>
    </h3>

    <p class="research-dates">
      📅 2019–2022
    </p>

    <p>
      Phonetic documentation of segmental and prosodic variation in
      contemporary Italian dialects, based on fieldwork and corpus data.
    </p>

    <p class="research-tags">
      🏷️
      <span class="research-tag">dialectology</span>
      <span class="research-tag">phonetics</span>
      <span class="research-tag">Italian dialects</span>
    </p>

    <p class="research-meta">
      👥 <strong>Collaborators:</strong> Luca Bianchi (Padua)
    </p>

    <p class="research-meta">
      💰 <strong>Funding:</strong> —
    </p>

    <p class="research-meta">
      📚 <strong>Published in:</strong> <em>Lingua</em> (2021)
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
      card.style.display =
        value === "all" || tags.includes(value) ? "" : "none";
    });

    status.textContent =
      value === "all"
        ? ""
        : "Showing projects tagged with: “" + value + "”.";
  });
});
</script>
