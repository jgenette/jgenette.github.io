---
title: "PhD Defence - English Translation"
layout: single-portfolio
excerpt: "<img src='/images/research/kaft.png' alt=''>"
permalink: /research/defense-en/
collection: research
order_number: 1
header: 
  og_image: "research/kaft.png"
---

<style>
  body {
    font-family: Arial, sans-serif;
    text-align: center;
    margin: 2rem;
  }
  #slideTitle {
    font-size: 2rem;
    margin-bottom: 1.5rem;
  }
  #controls {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 1.5rem;
  }
  button {
    background: #007bff;
    border: none;
    color: white;
    padding: 1rem 2rem;
    font-size: 1.5rem;
    border-radius: 8px;
    cursor: pointer;
    transition: background-color 0.3s ease;
    min-width: 120px;
  }
  button:hover:not(:disabled) {
    background: #0056b3;
  }
  button:disabled {
    background: #cccccc;
    cursor: not-allowed;
  }
</style>

<h2 id="slideTitle">Slide 1</h2>

<div id="controls">
  <button id="prevBtn" disabled>⬅️ Prev</button>
  <button id="playBtn">▶️ Play</button>
  <button id="nextBtn">Next ➡️</button>
</div>

<audio id="audio"></audio>

<script>
  const slides = [
    { title: "Slide 1", src: "/files/test.wav" },
    { title: "Slide 2", src: "/files/test.wav" },
    { title: "Slide 3", src: "/files/test.wav" }
  ];

  let currentSlide = 0;
  const slideTitle = document.getElementById('slideTitle');
  const audio = document.getElementById('audio');
  const playBtn = document.getElementById('playBtn');
  const prevBtn = document.getElementById('prevBtn');
  const nextBtn = document.getElementById('nextBtn');

  function updateUI() {
    slideTitle.textContent = slides[currentSlide].title;
    audio.src = slides[currentSlide].src;
    audio.load();
    playBtn.textContent = "▶️ Play";

    prevBtn.disabled = currentSlide === 0;
    nextBtn.disabled = currentSlide === slides.length - 1;
  }

  playBtn.addEventListener('click', () => {
    if (audio.paused) {
      audio.play();
      playBtn.textContent = "⏸️ Pause";
    } else {
      audio.pause();
      playBtn.textContent = "▶️ Play";
    }
  });

  prevBtn.addEventListener('click', () => {
    if (currentSlide > 0) {
      audio.pause();
      currentSlide--;
      updateUI();
    }
  });

  nextBtn.addEventListener('click', () => {
    if (currentSlide < slides.length - 1) {
      audio.pause();
      currentSlide++;
      updateUI();
    }
  });

  audio.addEventListener('ended', () => {
    playBtn.textContent = "▶️ Play";
    // Move to next slide visually but DO NOT auto-play
    if (currentSlide < slides.length - 1) {
      currentSlide++;
      updateUI();
    }
  });

  // Initialize UI on load
  updateUI();
</script>

