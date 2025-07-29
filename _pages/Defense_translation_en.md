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
<button id="play1">Play</button>

<!-- Slide 2 -->
<h3>Slide 2</h3>
<button id="play2" disabled>Play</button>

<!-- Slide 3 -->
<h3>Slide 3</h3>
<button id="play3" disabled>Play</button>

<audio id="audio1" src="/files/test.wav"></audio>
<audio id="audio2" src="/files/test.wav"></audio>
<audio id="audio3" src="/files/test.wav"></audio>

<script>
  const play1 = document.getElementById('play1');
  const play2 = document.getElementById('play2');
  const play3 = document.getElementById('play3');

  const audio1 = document.getElementById('audio1');
  const audio2 = document.getElementById('audio2');
  const audio3 = document.getElementById('audio3');

  // Play button for slide 1
  play1.addEventListener('click', () => {
    audio1.currentTime = 0;
    audio1.play();
    play1.disabled = true;
  });

  // Play button for slide 2
  play2.addEventListener('click', () => {
    audio2.currentTime = 0;
    audio2.play();
    play2.disabled = true;
  });

  // Play button for slide 3
  play3.addEventListener('click', () => {
    audio3.currentTime = 0;
    audio3.play();
    play3.disabled = true;
  });

  // When audio1 ends, enable play button for slide 2
  audio1.addEventListener('ended', () => {
    play2.disabled = false;
  });

  // When audio2 ends, enable play button for slide 3
  audio2.addEventListener('ended', () => {
    play3.disabled = false;
  });

  // When audio3 ends, optionally do something, like reset all buttons:
  audio3.addEventListener('ended', () => {
    play1.disabled = false;
    play2.disabled = true;
    play3.disabled = true;
  });
</script>
