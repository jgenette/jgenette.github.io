---
title: "Défense de thèse - Traduction française"
layout: single-portfolio
excerpt: "<img src='/images/research/kaft.png' alt=''>"
collection: research
permalink: /research/defense-fr/
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
  { title: "Diapositive 1", src: "/files/fr1.wav" },
  { title: "Diapositive 2", src: "/files/fr2.wav" },
  { title: "Diapositive 3", src: "/files/fr3.wav" },
  { title: "Diapositive 4", src: "/files/fr4.wav" },
  { title: "Diapositive 5", src: "/files/fr5.wav" },
  { title: "Diapositive 6", src: "/files/fr6.wav" },
  { title: "Diapositive 7", src: "/files/fr7.wav" },
  { title: "Diapositive 8", src: "/files/fr8.wav" },
  { title: "Diapositive 9", src: "/files/fr9.wav" },
  { title: "Diapositive 10", src: "/files/fr10.wav" },
  { title: "Diapositive 11", src: "/files/fr11.wav" },
  { title: "Diapositive 12", src: "/files/fr12.wav" },
  { title: "Diapositive 13", src: "/files/fr13.wav" },
  { title: "Diapositive 14", src: "/files/fr14.wav" },
  { title: "Diapositive 15", src: "/files/fr15.wav" },
  { title: "Diapositive 16", src: "/files/fr16.wav" },
  { title: "Diapositive 17", src: "/files/fr17.wav" },
  { title: "Diapositive 18", src: "/files/fr18.wav" },
  { title: "Diapositive 19", src: "/files/fr19.wav" },
  { title: "Diapositive 20", src: "/files/fr20.wav" },
  { title: "Diapositive 21", src: "/files/fr21.wav" },
  { title: "Diapositive 22", src: "/files/fr22.wav" },
  { title: "Diapositive 23", src: "/files/fr23.wav" },
  { title: "Diapositive 24", src: "/files/fr24.wav" },
  { title: "Diapositive 25", src: "/files/fr25.wav" },
  { title: "Diapositive 26", src: "/files/fr26.wav" },
  { title: "Diapositive 27", src: "/files/fr27.wav" },
  { title: "Diapositive 28", src: "/files/fr28.wav" }

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
