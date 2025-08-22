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
<title>Audio Slides Themed</title>
<style>
  /* Base variables from your theme */
  :root {
    --font-family: -apple-system, ".SFNSText-Regular", "San Francisco", Roboto, "Segoe UI", "Helvetica Neue", Arial, sans-serif;
    --font-size-base: 14px;
    --primary-color: #7D502E;
    --dark-gray: #4a4439;
    --light-gray: #ddd6c7;
    --background-color: #F6F1E0;
    --border-radius: 15px;
    --button-padding-vertical: 0.6rem;
    --button-padding-horizontal: 1.2rem;
  }

  /* Reset and base */
  body {
    font-family: var(--font-family);
    font-size: var(--font-size-base);
    color: var(--dark-gray);
    background-color: var(--background-color);
    margin: 3rem 1rem;
    text-align: center;
  }

  #slideTitle {
    font-size: 1.563em; /* type-size-3 ~25px */
    font-weight: 600;
    margin-bottom: 1.5rem;
  }

  #controls {
    margin-bottom: 2rem;
  }

  #controls button {
    font-size: 1.2rem;
    padding: var(--button-padding-vertical) var(--button-padding-horizontal);
    margin: 0 0.4rem;
    min-width: 80px;
    border-radius: var(--border-radius);
    border: 2px solid var(--primary-color);
    background-color: white;
    color: var(--primary-color);
    cursor: pointer;
    user-select: none;
    transition: background-color 0.25s ease, color 0.25s ease, box-shadow 0.25s ease;
    box-shadow: 0 1px 1px rgba(0,0,0,0.125);
  }

  #controls button:hover:not(:disabled) {
    background-color: var(--primary-color);
    color: white;
    box-shadow: 0 4px 6px rgba(125, 80, 46, 0.4);
  }

  #controls button:disabled {
    border-color: var(--light-gray);
    color: var(--light-gray);
    background-color: #f0ece4;
    cursor: default;
    box-shadow: none;
  }

  #controls button:focus {
    outline: 3px solid rgba(125, 80, 46, 0.5);
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
  { title: "Slide 1", src: "/files/en1.wav" },
  { title: "Slide 2", src: "/files/en2.wav" },
  { title: "Slide 3", src: "/files/en3.wav" },
  { title: "Slide 4", src: "/files/en4.wav" },
  { title: "Slide 5", src: "/files/en5.wav" },
  { title: "Slide 6", src: "/files/en6.wav" },
  { title: "Slide 7", src: "/files/en7.wav" },
  { title: "Slide 8", src: "/files/en8.wav" },
  { title: "Slide 9", src: "/files/en9.wav" },
  { title: "Slide 10", src: "/files/en10.wav" },
  { title: "Slide 11", src: "/files/en11.wav" },
  { title: "Slide 12", src: "/files/en12.wav" },
  { title: "Slide 13", src: "/files/en13.wav" },
  { title: "Slide 14", src: "/files/en14.wav" },
  { title: "Slide 15", src: "/files/en15.wav" },
  { title: "Slide 16", src: "/files/en16.wav" },
  { title: "Slide 17", src: "/files/en17.wav" },
  { title: "Slide 18", src: "/files/en18.wav" },
  { title: "Slide 19", src: "/files/en19.wav" },
  { title: "Slide 20", src: "/files/en20.wav" },
  { title: "Slide 21", src: "/files/en21.wav" },
  { title: "Slide 22", src: "/files/en22.wav" },
  { title: "Slide 23", src: "/files/en23.wav" },
  { title: "Slide 24", src: "/files/en24.wav" },
  { title: "Slide 25", src: "/files/en25.wav" },
  { title: "Slide 26", src: "/files/en26.wav" },
  { title: "Slide 27", src: "/files/en27.wav" },
  { title: "Slide 28", src: "/files/en28.wav" }
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
