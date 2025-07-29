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

<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Audio Slides</title>
<style>
  body {
    font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
    text-align: center;
    margin: 3rem 1rem;
    background-color: #f9fafb;
    color: #333;
  }
  #slideTitle {
    font-size: 2rem;
    margin-bottom: 1.5rem;
    font-weight: 600;
  }
  #controls {
    margin-bottom: 2rem;
  }
  #controls button {
    font-size: 1.2rem;
    padding: 0.6rem 1.2rem;
    margin: 0 0.4rem;
    min-width: 80px;
    border: 2px solid #4a90e2;
    border-radius: 6px;
    background-color: white;
    color: #4a90e2;
    cursor: pointer;
    transition: background-color 0.25s ease, color 0.25s ease;
    user-select: none;
  }
  #controls button:hover:not(:disabled) {
    background-color: #4a90e2;
    color: white;
  }
  #controls button:disabled {
    border-color: #cbd5e1;
    color: #cbd5e1;
    cursor: default;
    background-color: #f1f5f9;
  }
  #controls button:focus {
    outline: 3px solid #a0c4ff;
    outline-offset: 2px;
  }
</style>
</head>
<body>

<h2 id="slideTitle">Slide 1</h2>

<div id="controls">
  <button id="prevBtn" disabled>Prev</button>
  <button id="playBtn">Play</button>
  <button id="nextBtn">Next</button>
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
    playBtn.textContent = "Play";

    prevBtn.disabled = currentSlide === 0;
    nextBtn.disabled = currentSlide === slides.length - 1;
  }

  playBtn.addEventListener('click', () => {
    if (audio.paused) {
      audio.play();
      playBtn.textContent = "Pause";
    } else {
      audio.pause();
      playBtn.textContent = "Play";
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
    playBtn.textContent = "Play";
    if (currentSlide < slides.length - 1) {
      currentSlide++;
      updateUI();
    }
  });

  window.addEventListener('DOMContentLoaded', () => {
    updateUI();
  });
</script>

</body>
</html>


