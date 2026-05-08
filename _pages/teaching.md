---
permalink: /teaching/
layout: single
sidebar: false
author_profile: false
toc: false
header: 
  image: teachning_banner.png
---
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
  <title>Teaching & Courses · Phonetics Lab</title>
  <style>
    /* ===== RESET & GLOBAL ===== */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', sans-serif;
      background: #ffffff;
      color: #1e2a3a;
      line-height: 1.5;
    }

    .page-wrapper {
      max-width: 1200px;
      margin: 0 auto;
      padding: 2rem 1.5rem;
    }

    /* typography */
    h1 {
      font-size: 2.2rem;
      font-weight: 600;
      letter-spacing: -0.01em;
      margin-bottom: 0.5rem;
      color: #0f2b3d;
    }

    h2 {
      font-size: 1.75rem;
      font-weight: 600;
      margin: 2rem 0 1rem 0;
      padding-bottom: 0.4rem;
      border-bottom: 3px solid #e6eef2;
      color: #1e4663;
    }

    h3 {
      font-size: 1.3rem;
      font-weight: 600;
      margin-top: 0;
      margin-bottom: 0.5rem;
      color: #1e4663;
    }

    a {
      color: #2c7da0;
      text-decoration: none;
      transition: color 0.2s ease;
    }

    a:hover {
      color: #0f4c5f;
      text-decoration: underline;
    }

    hr {
      margin: 1.5rem 0;
      border: none;
      border-top: 1px solid #e2e8f0;
    }

    /* ===== HEADER BANNER ===== */
    .teaching-header {
      margin-bottom: 2rem;
    }

    .banner-image {
      width: 100%;
      max-height: 280px;
      object-fit: cover;
      border-radius: 24px;
      box-shadow: 0 8px 20px rgba(0,0,0,0.05);
      display: block;
    }

    /* ===== OBJECTIVES SECTION ===== */
    .objectives-card {
      background: #f8fafc;
      border-radius: 24px;
      padding: 1.6rem 2rem;
      margin: 1.8rem 0 2rem 0;
      border: 1px solid #e2edf2;
    }

    .objectives-card h2 {
      margin-top: 0;
      border-bottom: none;
      padding-bottom: 0;
    }

    .objectives-card ul {
      margin: 0.8rem 0 0 1.4rem;
    }

    .objectives-card li {
      margin: 0.4rem 0;
    }

    /* ===== COURSE GRID (cards consistent with research layout) ===== */
    .courses-grid {
      display: flex;
      flex-direction: column;
      gap: 1.8rem;
      margin: 1rem 0 2rem 0;
    }

    /* card style — like research-card but adjusted for teaching */
    .course-card {
      background-color: #ffffff;
      border: 1px solid #e2edf2;
      border-radius: 20px;
      padding: 1.5rem;
      display: flex;
      gap: 1.8rem;
      align-items: flex-start;
      transition: box-shadow 0.2s, transform 0.1s;
      box-shadow: 0 2px 5px rgba(0,0,0,0.02);
    }

    .course-card:hover {
      box-shadow: 0 12px 24px -12px rgba(0, 32, 64, 0.12);
      border-color: #cbdde6;
    }

    .course-content {
      flex: 1;
    }

    .course-media {
      flex: 0 0 220px;
    }

    .course-media img {
      width: 100%;
      height: auto;
      aspect-ratio: 220 / 140;
      object-fit: cover;
      border-radius: 16px;
      background: #f1f5f9;
      box-shadow: 0 2px 6px rgba(0,0,0,0.05);
      display: block;
    }

    .course-meta {
      font-size: 0.85rem;
      color: #4a6a7f;
      margin: 0.2rem 0 0.6rem 0;
      display: flex;
      flex-wrap: wrap;
      gap: 0.8rem;
    }

    .course-meta span {
      background: #eff3f6;
      padding: 0.2rem 0.6rem;
      border-radius: 20px;
      display: inline-block;
      font-size: 0.75rem;
      font-weight: 500;
    }

    .course-description {
      margin: 0.8rem 0;
      color: #2c3e4e;
    }

    .course-links {
      margin-top: 0.8rem;
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
      font-size: 0.85rem;
    }

    .course-links a {
      background: #eef3f8;
      padding: 0.2rem 0.8rem;
      border-radius: 24px;
      display: inline-block;
      font-weight: 500;
    }

    .course-links a:hover {
      background: #e0eef6;
      text-decoration: none;
    }

    /* featured course (first one with banner style) */
    .featured-course-card {
      background: #fefefc;
      border-left: 5px solid #2c7da0;
    }

    /* resources list */
    .resources-list {
      background: #f9fbfd;
      border-radius: 20px;
      padding: 1.5rem 2rem;
      margin-top: 1rem;
      border: 1px solid #e6edf2;
    }

    .resources-list ul {
      margin-left: 1.4rem;
      margin-top: 0.5rem;
    }

    .resources-list li {
      margin: 0.6rem 0;
    }

    /* filter info (from research page, optional) */
    .filter-info {
      background: #f1f6f9;
      border-radius: 40px;
      display: inline-block;
      padding: 0.3rem 1rem;
      font-size: 0.8rem;
      margin-bottom: 1rem;
      color: #2c6280;
    }

    /* responsive */
    @media (max-width: 780px) {
      .page-wrapper {
        padding: 1.2rem;
      }
      .course-card {
        flex-direction: column;
      }
      .course-media {
        flex: none;
        width: 100%;
      }
      .course-media img {
        max-height: 180px;
        width: 100%;
        object-fit: cover;
      }
      .objectives-card {
        padding: 1.2rem;
      }
      h2 {
        font-size: 1.5rem;
      }
    }

    @media (max-width: 500px) {
      .course-links {
        flex-direction: column;
        gap: 0.4rem;
      }
    }

    /* subtle circle decoration (clean) */
    .tag {
      font-size: 0.7rem;
      background: #e9f0f5;
      padding: 0.2rem 0.6rem;
      border-radius: 30px;
      display: inline-block;
      color: #2c6280;
    }
  </style>
</head>
<body>
<div class="page-wrapper">

  <!-- HEADER with banner (improved from teachning_banner.png) -->
  <div class="teaching-header">
    <img class="banner-image" src="/assets/images/teaching/teachning_banner.png" alt="Phonetics classroom and lab banner" onerror="this.src='https://placehold.co/1200x280/eef2f5/2c7da0?text=Speech+Acoustics+Lab'; this.onerror=null;">
  </div>

  <!-- OBJECTIVES SECTION (refined card + more detail) -->
  <div class="objectives-card">
    <h2>📖 Objectives in the Classroom</h2>
    <p>In my courses, students actively engage with phonetic inquiry, data analysis, and theoretical reflection. You can expect:</p>
    <ul>
      <li>🔊 <strong>Hands-on acoustic analysis</strong> – from recording to spectrogram interpretation using Praat and Python.</li>
      <li>📊 <strong>Real speech corpora</strong> – child, clinical, and multilingual data to connect theory with empirical evidence.</li>
      <li>🧠 <strong>Active learning & discussion</strong> – lab-based sessions, peer review of phonetic annotations, and problem sets in laboratory phonology.</li>
      <li>📑 <strong>Reproducible research practices</strong> – transparent workflows, open materials, and collaborative data challenges.</li>
    </ul>
  </div>

  <!-- COURSES TAUGHT (grid with card design, mirroring research layout) -->
  <h2>📚 Courses taught</h2>
  <div class="courses-grid" id="courses-container">

    <!-- COURSE 1 – Phonetics & Phonology (featured / graduate) -->
    <div class="course-card featured-course-card">
      <div class="course-content">
        <h3>Phonetics and Phonology</h3>
        <div class="course-meta">
          <span>🗓️ Spring 2026</span>
          <span>📍 KU Leuven, BE</span>
          <span>🎓 Graduate level</span>
          <span>👩‍🏫 University lecturer</span>
        </div>
        <p class="course-description">
          This MA-level course provides an integrated introduction to articulatory and acoustic phonetics and core issues in phonological theory. 
          Students learn to analyse speech acoustically, interpret spectrograms, and connect empirical observations to theoretical questions in phonology — 
          with lab sessions on cue-weighting and vowel space analysis.
        </p>
        <div class="course-links">
          <a href="/assets/syllabus/phonetics_phonology_syllabus.pdf">📄 Syllabus (PDF)</a>
          <a href="/assets/assignments/phonetics_phonology_lab1.zip">🧪 Lab materials</a>
          <a href="#">📊 Praat scripts</a>
        </div>
      </div>
      <div class="course-media">
        <img src="/assets/images/teaching/phonetics_and_phonology.png" alt="Phonetics and Phonology banner" onerror="this.src='https://placehold.co/220x140/d9e6f2/2c7da0?text=phonetics+lab'">
      </div>
    </div>

    <!-- COURSE 2 – French Orthography -->
    <div class="course-card">
      <div class="course-content">
        <h3>Orthographe lexicale et grammaticale <span style="font-weight:normal;">[French Lexical & Grammatical Orthography]</span></h3>
        <div class="course-meta">
          <span>🍂 Fall 2025</span>
          <span>📍 Université de Mons, BE</span>
          <span>🎓 Undergraduate</span>
          <span>👩‍🏫 Lecturer</span>
        </div>
        <p class="course-description">
          Exploration of French spelling systems, morphophonological alternations, and didactic approaches. Students analyze spelling errors in L1 and L2 corpora, linking orthographic conventions to phonological patterns.
        </p>
        <div class="course-links">
          <a href="#">📘 Course outline</a>
          <a href="#">📝 Error analysis toolkit</a>
        </div>
      </div>
      <div class="course-media">
        <img src="/assets/images/teaching/french-orthography.png" alt="French orthography materials" onerror="this.src='https://placehold.co/220x140/e6f0f5/2c7da0?text=french+orthography'">
      </div>
    </div>

    <!-- COURSE 3 – General Linguistics -->
    <div class="course-card">
      <div class="course-content">
        <h3>Linguistique générale [General Linguistics]</h3>
        <div class="course-meta">
          <span>🍂 Fall 2025</span>
          <span>📍 Université de Mons, BE</span>
          <span>🎓 Undergraduate</span>
          <span>👩‍🏫 Lecturer</span>
        </div>
        <p class="course-description">
          Introduction to core areas: phonetics, phonology, morphology, syntax, semantics, and pragmatics. Emphasis on cross-linguistic data and empirical reasoning. Includes a practical module on phonetic transcription and acoustic analysis of regional varieties.
        </p>
        <div class="course-links">
          <a href="#">📖 Reading list</a>
          <a href="#">🎧 Speech dataset</a>
        </div>
      </div>
      <div class="course-media">
        <img src="/assets/images/teaching/general-linguistics.png" alt="General linguistics" onerror="this.src='https://placehold.co/220x140/eef3f7/2c7da0?text=linguistics'">
      </div>
    </div>

    <!-- COURSE 4 – Audiology guest lecture (Wrocław) -->
    <div class="course-card">
      <div class="course-content">
        <h3>Module Audiology, Acoustic Phonetics and Deafness</h3>
        <div class="course-meta">
          <span>📅 23 October 2025</span>
          <span>📍 Uniwersytet Wrocławski, PL</span>
          <span>🎤 Guest lecture</span>
        </div>
        <p class="course-description">
          <em>“Corpora en wetenschappelijk onderzoek in de taalkunde”</em> [Corpora and scientific research in linguistics, in Dutch]. Focus on using large-scale speech corpora to investigate phonetic variation in hearing-impaired and typically developing populations.
        </p>
        <div class="course-links">
          <a href="#">📑 Lecture slides</a>
          <a href="#">📊 Corpus tutorial</a>
        </div>
      </div>
      <div class="course-media">
        <img src="/assets/images/teaching/audiology.png" alt="Audiology and acoustic phonetics" onerror="this.src='https://placehold.co/220x140/e0edf5/2c7da0?text=audiology+module'">
      </div>
    </div>

    <!-- COURSE 5 – Audiology guest lecture (London) -->
    <div class="course-card">
      <div class="course-content">
        <h3>Module Audiology, Acoustic Phonetics and Deafness</h3>
        <div class="course-meta">
          <span>📅 11 September 2025</span>
          <span>📍 City, St George’s, University of London, UK</span>
          <span>🎤 Guest lecture</span>
        </div>
        <p class="course-description">
          <em>“The developmental aspect(s) of Intrinsic Vowel Pitch”</em> — how vocal fold tension and vowel height interact in child speech, with evidence from deaf and hearing infants. Discussion of clinical implications for paediatric audiology.
        </p>
        <div class="course-links">
          <a href="#">📊 Experimental data</a>
          <a href="#">🎥 Recording</a>
        </div>
      </div>
      <div class="course-media">
        <img src="/assets/images/teaching/audiology.png" alt="Intrinsic vowel pitch lecture" onerror="this.src='https://placehold.co/220x140/e9f0f4/2c7da0?text=IVP+research'">
      </div>
    </div>

    <!-- COURSE 6 – BA Thesis supervision -->
    <div class="course-card">
      <div class="course-content">
        <h3>Bachelorscriptie [BA thesis]</h3>
        <div class="course-meta">
          <span>📅 2024 – 2026</span>
          <span>📍 Universiteit Antwerpen, BE</span>
          <span>🎓 Undergraduate (Assessor)</span>
        </div>
        <p class="course-description">
          Assessment and supervision of BA theses in Applied Linguistics, with special attention to experimental phonetics, corpus-based research, and replication studies. Guidance on methodology, acoustic annotation, and statistical reporting.
        </p>
        <div class="course-links">
          <a href="#">📌 Thesis guidelines</a>
          <a href="#">📁 Template repository</a>
        </div>
      </div>
      <div class="course-media">
        <img src="/assets/images/teaching/ba-thesis.png" alt="BA thesis supervision" onerror="this.src='https://placehold.co/220x140/f1f6fa/2c7da0?text=BA+thesis'">
      </div>
    </div>

    <!-- Additional Guest Lecture (optional from CV: Mannheim / ULB) shown as extra demonstration of consistency -->
    <div class="course-card">
      <div class="course-content">
        <h3>Speech development across populations (Guest lecture)</h3>
        <div class="course-meta">
          <span>🗓️ March 2025</span>
          <span>📍 Universität Mannheim, DE</span>
          <span>🎤 Invited talk</span>
        </div>
        <p class="course-description">
          “Acoustic correlates of phonological development in cochlear-implanted children”: cross-linguistic comparison of vowel space and f0 patterns. Emphasis on reproducibility and open science frameworks.
        </p>
        <div class="course-links">
          <a href="#">🔗 Preprint</a>
          <a href="#">📈 Data repository</a>
        </div>
      </div>
      <div class="course-media">
        <img src="/assets/images/teaching/mannheim_talk.png" alt="Guest lecture Mannheim" onerror="this.src='https://placehold.co/220x140/cfe3ef/2c7da0?text=Mannheim+guest+talk'">
      </div>
    </div>
  </div>

  <!-- USEFUL LINKS / RESOURCES (styled as a modern grid) -->
  <h2>🔗 Useful links & student resources</h2>
  <div class="resources-list">
    <p><strong>Selected tools, tutorials, and corpora for phonetic research:</strong></p>
    <ul>
      <li><a href="https://www.fon.hum.uva.nl/praat/" target="_blank" rel="noopener">🎙️ Praat (speech analysis)</a> – scripting tutorials & manual</li>
      <li><a href="https://jgenette.shinyapps.io/colouringtheillustrationapp/" target="_blank" rel="noopener">🎨 IPA chart designer</a> – interactive custom charts</li>
      <li><a href="https://childes.talkbank.org/" target="_blank" rel="noopener">👶 CHILDES corpus</a> – child language data, clinical & longitudinal</li>
      <li><a href="https://github.com/opensource-phonetics/voice" target="_blank" rel="noopener">📦 Python for phonetics (Parselmouth, PraatIO)</a></li>
      <li><a href="#">📊 Statistical workflows in R (lme4, phonTools)</a> – code and examples from courses</li>
    </ul>
    <p style="margin-top: 0.8rem; font-size:0.9rem;">📌 <em>More tutorials and lab exercises available on the course GitHub organization.</em></p>
  </div>

  <!-- FOOTER note (optional) -->
  <hr>
  <p style="font-size:0.85rem; color:#5f7f95; text-align:center; margin-top:2rem;">
    📢 Open teaching materials — all resources are shared under CC BY‑NC 4.0 license. 
    <br>For questions about assignments or access to lab data, please <a href="/contact">get in touch</a>.
  </p>
</div>

<!-- Simple filter & interactive enhancement (like research page but adapted for teaching) -->
<script>
  (function() {
    // Add a category filter to match research page style? 
    // We'll add a dynamic filter for course types (graduate/undergraduate/guest) as an optional upgrade
    const container = document.getElementById('courses-container');
    if (!container) return;
    
    // Create filter bar above courses (similar to research experience)
    const filterWrapper = document.createElement('div');
    filterWrapper.className = 'research-filter';
    filterWrapper.style.marginBottom = '1rem';
    filterWrapper.style.marginTop = '0.5rem';
    filterWrapper.innerHTML = `
      <label for="course-filter"><strong>🔍 Filter courses:</strong></label>
      <select id="course-filter" style="margin-left:0.6rem; padding:0.3rem 0.8rem; border-radius:30px; border:1px solid #cbdde6; background:white;">
        <option value="all">All courses</option>
        <option value="graduate">Graduate level</option>
        <option value="undergraduate">Undergraduate level</option>
        <option value="guest">Guest lectures</option>
        <option value="assessment">Assessment / thesis</option>
      </select>
      <span id="filter-feedback" style="margin-left:1rem; font-size:0.75rem; color:#4e7c97;"></span>
    `;
    
    const coursesTitle = document.querySelector('h2:contains("Courses taught")');
    function insertAfter(newNode, referenceNode) {
      referenceNode.parentNode.insertBefore(newNode, referenceNode.nextSibling);
    }
    // simple polyfill for :contains
    let targetHeader = null;
    const allH2 = document.querySelectorAll('h2');
    for (let h of allH2) {
      if (h.innerText.includes('Courses taught')) {
        targetHeader = h;
        break;
      }
    }
    if (targetHeader) {
      targetHeader.insertAdjacentElement('afterend', filterWrapper);
    } else {
      // fallback: prepend to courses grid parent
      const gridParent = container.parentNode;
      gridParent.insertBefore(filterWrapper, container);
    }

    const filterSelect = document.getElementById('course-filter');
    const cards = document.querySelectorAll('.course-card');
    const feedbackSpan = document.getElementById('filter-feedback');

    function updateFilter() {
      const value = filterSelect.value;
      let visibleCount = 0;
      cards.forEach(card => {
        let matches = false;
        const meta = card.querySelector('.course-meta')?.innerText || '';
        const title = card.querySelector('h3')?.innerText || '';
        const description = card.querySelector('.course-description')?.innerText || '';
        const combined = (meta + title + description).toLowerCase();

        if (value === 'all') matches = true;
        else if (value === 'graduate' && (combined.includes('graduate') || combined.includes('ma-level') || combined.includes('master'))) matches = true;
        else if (value === 'undergraduate' && (combined.includes('undergraduate') || combined.includes('ba') || combined.includes('licence'))) matches = true;
        else if (value === 'guest' && (combined.includes('guest lecture') || combined.includes('invited') || combined.includes('guest'))) matches = true;
        else if (value === 'assessment' && (combined.includes('thesis') || combined.includes('assessor') || combined.includes('bachelorscriptie'))) matches = true;
        
        if (matches) {
          card.style.display = '';
          visibleCount++;
        } else {
          card.style.display = 'none';
        }
      });
      if (feedbackSpan) {
        if (value === 'all') feedbackSpan.textContent = '';
        else feedbackSpan.textContent = `Showing ${visibleCount} course${visibleCount !== 1 ? 's' : ''}.`;
      }
    }
    if (filterSelect) filterSelect.addEventListener('change', updateFilter);
    updateFilter();
  })();

  // small helper to improve summary style if needed (borrow toggle elegance but not needed here)
  // Remove the broken ":contains" polyfill alternative by ensuring title selector works
  if (typeof window !== 'undefined' && !Element.prototype.matches) {
    // just a safety
  }
</script>

</body>
</html>
