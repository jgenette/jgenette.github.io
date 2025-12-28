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
  border-radius: 12px;
  padding: 1.25rem;
}

.research-card-image {
  margin-bottom: 0.75rem;
}

.research-card-image img {
  width: 100%;
  height: auto;
  border-radius: 8px;
}

.research-card h3 {
  margin-top: 0;
  margin-bottom: 0.25rem;
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

.research-tag {
  display: inline-block;
  margin-right: 0.6rem;
  color: #555;
}

.research-meta {
  font-size: 0.85rem;
  color: #444;
  margin: 0.3rem 0;
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

  <!-- PROJECT CARD -->
  <div class="research-card"
       data-tags="acoustics babbling child speech hearing impairment">

    <div class="research-card-image">
      <img src="/assets/images/research/babbling.jpg"
           alt="Spectrogram of early babbling">
    </div>

    <h3>
      <a href="/research/early-babbling/">
        Acoustic cue-weighting in Infant-Directed Speech
      </a>
    </h3>

    <p class="research-dates">📅 2025–present</p>

    <p>
      The proposed research project investigates how infants learn speech sound categories from the
linguistic input they receive: Infant-Directed Speech (IDS). Previous research has shown that speech
sounds are best distinguished by a combination of primary, essential cues and secondary, yet
informative, cues. However, research on IDS and early language acquisition has largely overlooked
the role of these secondary cues. Therefore, our understanding of IDS and its role in language
acquisition remains overly simplified. To address this lacuna, the present project aims to develop a
more comprehensive understanding of how speech sounds are phonetically contrasted through
multiple cues in IDS, whether this facilitates speech sound categorization, and how this affects
language acquisition.

For this purpose, we will combine large-scale corpus studies of spontaneous speech production with
perception experiments. Specifically, we will investigate (1) whether parents exaggerate a single
fundamental cue or a combination of cues to help children learn phonological categories through the
acoustic analysis of a corpus of parent-infant interactions, (2) we will test in the same corpus
whether variations in caregivers' cue-weighting can (partially) explain individual differences in the
infants' own cue-weighting in production and (3) we will examine how IDS cue-weighting shapes
phoneme categorization, bridging the caregiver input and infant output by means of targeted
perception experiments.
    </p>

    <p class="research-tags">
      🏷️ Acoustics · Language Acquisition · Acoustic Cue-Weighting · Dutch
    </p>

    <p class="research-meta">
      👥 <strong>Collaborators:</strong> Sarah Bernolet (University of Antwerp, BE), Jo Verhoeven (City St George's, University of London, UK)
    </p>

    <p class="research-meta">
      💰 <strong>Funding:</strong> The Research Foundation – Flanders (FWO) [1235526N]
    </p>

  </div>

  <!-- PROJECT CARD -->
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

    <p class="research-dates">📅 2021–2023</p>

    <p>
      Examination of methodological choices in acoustic analysis,
      annotation reliability, and reproducibility within a laboratory
      phonology framework.
    </p>

    <p class="research-tags">
      🏷️ phonetics · methods · laboratory phonology
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

  <!-- PROJECT CARD -->
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

    <p class="research-dates">📅 2019–2022</p>

    <p>
      Phonetic documentation of segmental and prosodic variation in
      contemporary Italian dialects, based on fieldwork and corpus data.
    </p>

    <p class="research-tags">
      🏷️ dialectology · phonetics · Italian dialects
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
