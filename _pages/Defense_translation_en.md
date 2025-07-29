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
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Simple Audio Slides</title>
<style>
  body {
    font-family: sans-serif;
    text-align: center;
    margin: 2rem;
  }
  #slideTitle {
    font-size: 1.8rem;
    margin-bottom: 1rem;
  }
  #controls button {
    font-size: 1.2rem;
    padding: 0.6rem 1.2rem;
    margin: 0 0.3rem;
    cursor: pointer;
  }
  #controls button:disabled {
    opacity: 0.5;
    cursor: default;
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


