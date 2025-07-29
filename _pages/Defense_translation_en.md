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

<!-- Slide 1 -->
<h3>Slide 1</h3>
<audio id="audio1" controls>
  <source src="/files/test.wav" type="audio/mpeg">
</audio>

<!-- Slide 2 -->
<h3>Slide 2</h3>
<audio id="audio2" controls>
  <source src="/files/test.wav" type="audio/mpeg">
</audio>

<!-- Slide 3 -->
<h3>Slide 3</h3>
<audio id="audio3" controls>
  <source src="/files/test.wav" type="audio/mpeg">
</audio>

<!-- Optional Reset Button -->
<button id="resetButton">Restart from Slide 1</button>

<script>
  const audio1 = document.getElementById("audio1");
  const audio2 = document.getElementById("audio2");
  const audio3 = document.getElementById("audio3");
  const resetButton = document.getElementById("resetButton");

  let current = 1;

  function pauseOthers(except) {
    [audio1, audio2, audio3].forEach(audio => {
      if (audio !== except) {
        audio.pause();
        audio.currentTime = 0;
      }
    });
  }

  audio1.addEventListener("play", () => {
    pauseOthers(audio1);
    current = 1;
  });

  audio2.addEventListener("play", () => {
    if (current >= 2) {
      pauseOthers(audio2);
      current = 2;
    } else {
      audio2.pause(); // block early access
    }
  });

  audio3.addEventListener("play", () => {
    if (current >= 3) {
      pauseOthers(audio3);
      current = 3;
    } else {
      audio3.pause(); // block early access
    }
  });

  // When one audio ends, enable the next step
  audio1.addEventListener("ended", () => current = 2);
  audio2.addEventListener("ended", () => current = 3);
  audio3.addEventListener("ended", () => current = 1);

  resetButton.addEventListener("click", () => {
    pauseOthers();
    current = 1;
  });
</script>
