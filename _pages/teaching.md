---
permalink: /teaching/
title: "Teaching"
excerpt: "Teaching"
author_profile: true
---

<!-- ===== HERO / BANNER (utilise votre image uploadée) -->
<section style="margin-bottom:20px;">
  <img src="/mnt/data/dc113963-eb37-4a22-86d5-84a900571906.png" alt="Teaching banner" style="width:100%; max-height:240px; object-fit:cover; border-radius:6px;">
</section>

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
  <article class="course">
    <div class="course-media">
      <!-- you can replace the src by a course-specific image -->
      <img src="/assets/images/teaching/phonetics-course.png" alt="Intro Phonetics" style="width:220px; height:140px; object-fit:cover; border-radius:6px;">
    </div>
    <div class="course-content">
      <h3>Introduction to Phonetics (BA / MA)</h3>
      <p><strong>When:</strong> Fall 20XX — <strong>Where:</strong> Universiteit Antwerpen</p>
      <p>Lecture-based introduction to articulatory and acoustic phonetics. Topics include speech production, acoustic correlates of segments, basic spectrogram interpretation and experimental methods. Assignments include lab exercises using Praat and short data projects.</p>
      <p><a href="/assets/syllabus/intro-phonetics-syllabus.pdf">Syllabus (PDF)</a> · <a href="/assets/assignments/phonetics-lab1.zip">Lab materials</a></p>
    </div>
  </article>

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
  <h2>Resources & Reading Lists</h2>
  <p>Selected resources for students (tools, tutorials, corpora):</p>
  <ul>
    <li><a href="https://www.fon.hum.uva.nl/praat/">Praat tutorials</a></li>
    <li><a href="/assets/reading-lists/quantitative-phonetics.md">Quantitative phonetics — reading list</a></li>
    <li><a href="/assets/links/corpora.md">Corpora & datasets</a></li>
  </ul>
</section>

<!-- ===== CONTACT / OFFICE HOURS -->
<section style="background:#f6f7f8; padding:14px; border-radius:6px; margin-top:18px;">
  <h2>Contact & Office hours</h2>
  <p>Email: <a href="mailto:your.name@university.edu">your.name@university.edu</a></p>
  <p>Office hours: Tue 14:00–16:00 (or by appointment). Location: <em>Add your office</em>.</p>
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
</style>
