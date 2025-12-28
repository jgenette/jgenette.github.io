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
/* Layout */
.research-grid {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

/* Card */
.research-card {
  background-color: #f5f5f5;
  border: 1px solid #e0e0e0;
  border-radius: 14px;
  padding: 1.5rem;
  display: flex;
  gap: 1.5rem;
  align-items: flex-start;
}

/* Text vs image */
.research-card-content {
  flex: 1;
}

.research-card-image {
  flex: 0 0 220px;
}

.research-card-image img {
  width: 100%;
  height: auto;
  border-radius: 10px;
}

/* Typography */
.research-card h3 {
  margin-top: 0;
  margin-bottom: 0.3rem;
}

.research-dates {
  font-size: 0.85rem;
  color: #666;
  margin-bottom: 0.6rem;
}

.research-tags {
  font-size: 0.75rem;
  margin: 0.6rem 0;
  color: #555;
}

.research-meta {
  font-size: 0.85rem;
  color: #444;
  margin: 0.3rem 0;
}

/* Filter */
.research-filter {
  margin-bottom: 1.5rem;
}

/* Summary toggle */
.research-summary {
  display: none;
  margin-top: 0.75rem;
}

.research-toggle {
  font-size: 0.8rem;
  color: #555;
  cursor: pointer;
  margin-top: 0.5rem;
  display: inline-block;
}

.research-toggle:hover {
  text-decoration: underline;
}

/* Responsive */
@media (max-width: 700px) {
  .research-card {
    flex-direction: column;
  }

  .research-card-image {
    flex: none;
  }
}
</style>

<!-- ===================== -->
<!-- Research intro       -->
<!-- ===================== -->

<p>
My research focuses on the acoustic and phonetic properties of child speech,
with particular attention to hearing impairment, laboratory phonology,
and methodological issues in speech sciences.
</p>

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
    <option value="language acquisition">Language Acquisition</option>
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

  <!-- PROJECT -->
  <div class="research-card"
       data-tags="acoustics language acquisition phonetics">

    <div class="research-card-content">

      <h3>
        <a href="/research/ids-cue-weighting/">
          Acoustic cue-weighting in Infant-Directed Speech
        </a>
      </h3>

      <p class="research-dates">📅 2025–present</p>

      <p class="research-tags">
        🏷️ Acoustics · Language acquisition · Cue-weighting · Dutch
      </p>

      <p class="research-meta">
        👥 <strong>Collaborators:</strong>
        Sarah Bernolet (University of Antwerp, BE),
        Jo Verhoeven (City St George’s, University of London, UK)
      </p>

      <p class="research-meta">
        💰 <strong>Funding:</strong>
        Research Foundation – Flanders (FWO) [1235526N]
      </p>

      <span class="research-toggle" onclick="toggleSummary(this)">
        ▶ Show summary
      </span>

      <div class="research-summary">
        <p>
          This project investigates how infants learn speech sound categories
          from Infant-Directed Speech (IDS), focusing on the role of secondary
          acoustic cues that have been largely overlooked in previous research.
        </p>

        <p>
          Combining large-scale corpus analyses of parent–infant interactions
          with perception experiments, the project examines cue-weighting in
          caregiver input and its relationship with infant production and
          categorization.
        </p>
      </div>

    </div>

    <div class="research-card-image">
      <img src="/assets/images/research/babbling.jpg"
           alt="Spectrogram of infant-directed speech">
    </div>

  </div>

  <!-- PROJECT -->
  <div class="research-card"
       data-tags="phonetics methods">

    <div class="research-card-content">

      <h3>
        <a href="/research/phonetic-methods/">
          Methodological issues in child speech phonetics
        </a>
      </h3>

      <p class="research-dates">📅 2021–2023</p>

      <p class="research-tags">
        🏷️ Phonetics · Methods · Laboratory phonology
      </p>

      <p class="research-meta">
        🎤 <strong>Presented at:</strong> LabPhon 18 (2022)
      </p>

      <span class="research-toggle" onclick="toggleSummary(this)">
        ▶ Show summary
      </span>

      <div class="research-summary">
        <p>
          This project examined methodological choices in acoustic analysis,
          annotation practices, and reproducibility in child speech research
          within a laboratory phonology framework.
        </p>
      </div>

    </div>

    <div class="research-card-image">
      <img src="/assets/images/research/methods.jpg"
           alt="Acoustic analysis workflow">
    </div>

  </div>

  <!-- PROJECT -->
  <div class="research-card"
       data-tags="dialectology phonetics">

    <div class="research-card-content">

      <h3>
        <a href="/research/italian-dialectology/">
          Phonetic variation in Italian dialects
        </a>
      </h3>

      <p class="research-dates">📅 2019–2022</p>

      <p class="research-tags">
        🏷️ Dialectology · Phonetics · Italian dialects
      </p>

      <p class="research-meta">
        📚 <strong>Published in:</strong> <em>Lingua</em> (2021)
      </p>

    </div>

    <div class="research-card-image">
      <img src="/assets/images/research/dialectology.jpg"
           alt="Italian dialect map">
    </div>

  </div>

</div>

<!-- ===================== -->
<!-- Scripts              -->
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

function toggleSummary(button) {
  const summary = button.nextElementSibling;

  if (summary.style.display === "block") {
    summary.style.display = "none";
    button.textContent = "▶ Show summary";
  } else {
    summary.style.display = "block";
    button.textContent = "▼ Hide summary";
  }
}
</script>
