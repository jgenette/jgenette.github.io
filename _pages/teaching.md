---
permalink: /teaching/
title: "Teaching"
excerpt: "Teaching"
layout: single
sidebar: false
author_profile: false
toc: false
header:
  overlay_image: "/assets/images/teaching/phonetics_and_phonology.png"
  show_overlay_title: false
---

<!-- ===== OBJECTIVES -->
<section>
  <h2>Objectives in the Classroom</h2>
  <p>In my courses, students can expect to:</p>
  <ul>
    <li>Get hands-on experience with acoustic analysis and speech data</li>
    <li>Learn quantitative methods used in laboratory phonology and speech sciences</li>
    <li>Develop skills in annotation, signal processing and statistical analysis</li>
    <li>Practice presenting and writing clear, evidence-based arguments</li>
    <li>Engage with both theoretical and applied topics in phonetics and language acquisition</li>
  </ul>
</section>

<!-- ===== COURSES (structure type "Alex Stern": image + description per course) -->
<section>
  <h2>Courses taught</h2>

<!-- Course 1 -->
<section class="course-block">

  <!-- FULL-WIDTH COURSE BANNER -->
  <img src="/assets/images/teaching/phonetics_and_phonology.png"
       alt="Phonetics and Phonology banner"
       class="course-banner">

  <!-- COURSE CONTENT -->
  <div class="course-content">
    <p><strong>When:</strong> Spring 2026 — <strong>Where:</strong> KU Leuven</p>

    <p>This MA-level course provides an integrated introduction to articulatory and acoustic
    phonetics and to core issues in phonological theory. Students learn to analyse speech
    acoustically, interpret spectrograms, and connect empirical observations to theoretical
    questions in phonology.</p>

    <p>
      <a href="/assets/syllabus/phonetics_phonology_syllabus.pdf">Syllabus (PDF)</a>
      ·
      <a href="/assets/assignments/phonetics_phonology_lab1.zip">Lab materials</a>
    </p>
  </div>

</section>


  <!-- Course 2 -->
  <article class="course">
    <div class="course-media">
      <img src="/assets/images/teaching/child-speech.png" alt="Child speech acoustics" style="width:220px; height:140px; object-fit:cover; border-radius:6px;">
    </div>
    <div class="course-content">
      <h3>Child Speech Acoustics (Graduate seminar)</h3>
      <p><strong>When:</strong> Spring 20XX — <strong>Where:</strong> Universiteit Antwerpen</p>
      <p>Advanced seminar centered on acoustic properties of babbling and early lexical production; includes reading of recent papers, replication work, and student projects analyzing longitudinal corpora.</p>
      <p><a href="/assets/syllabus/child-speech-syllabus.pdf">Syllabus (PDF)</a> · <a href="/assets/reading-lists/child-speech.md">Reading list</a></p>
    </div>
  </article>

  <!-- Course 3 -->
  <article class="course">
    <div class="course-media">
      <img src="/assets/images/teaching/methods.png" alt="Methods in speech sciences" style="width:220px; height:140px; object-fit:cover; border-radius:6px;">
    </div>
    <div class="course-content">
      <h3>Methods in Speech Sciences</h3>
      <p><strong>When:</strong> Occasional — <strong>Where:</strong> Guest lectures / workshops</p>
      <p>Hands-on workshops: Praat scripting, spectrogram analysis, annotation (ELAN) and reproducible pipelines (R / Python). Ideal for students preparing MSc projects or doctoral research.</p>
      <p><a href="/assets/workshops/methods-handout.pdf">Workshop handout</a></p>
    </div>
  </article>

  <!-- Course 4 (example dialectology seminar) -->
  <article class="course">
    <div class="course-media">
      <img src="/assets/images/teaching/dialectology.png" alt="Dialectology" style="width:220px; height:140px; object-fit:cover; border-radius:6px;">
    </div>
    <div class="course-content">
      <h3>Dialectology and Variation</h3>
      <p><strong>When:</strong> Spring 20XX — <strong>Where:</strong> KU Leuven (guest)</p>
      <p>Seminar on methods in dialectology: fieldwork design, sociolinguistic questionnaires, and acoustic measures of regional variation.</p>
      <p><a href="/assets/syllabus/dialectology-syllabus.pdf">Syllabus (PDF)</a></p>
    </div>
  </article>

</section>

<!-- ===== ADDITIONAL RESOURCES -->
<section>
  <h2>Useful links</h2>
  <p>Selected resources for students (tools, tutorials, corpora):</p>
  <ul>
    <li><a href="https://www.fon.hum.uva.nl/praat/">Praat tutorials</a></li>
    <li><a href="/assets/reading-lists/quantitative-phonetics.md">Quantitative phonetics — reading list</a></li>
    <li><a href="/assets/links/corpora.md">Corpora & datasets</a></li>
  </ul>
</section>


<!-- ===== CSS simple pour aligner les cours (responsive) -->
<style>
.course {
  display: flex;
  gap: 18px;
  margin: 18px 0;
  align-items: flex-start;
}
.course-media { flex: 0 0 220px; }
.course-content { flex: 1 1 auto; }

@media (max-width: 800px) {
  .course { flex-direction: column; }
  .course-media { width:100%; }
}

.course-banner {
  width: 100%;
  max-height: 260px;
  object-fit: cover;
  border-radius: 6px;
  display: block;
  margin-bottom: 15px;
}
.course-block {
  margin-top: 20px;
  margin-bottom: 40px;
}
</style>
</style>
