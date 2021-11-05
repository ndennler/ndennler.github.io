---
layout: post
title:  "Fashion Photoshoot with the Fashion Industry Association"
date:   2020-03-07 00:00:00
blurb: "The photoshoot we did before we were wrecked by COVID-19."
og_image: /assets/img/content/post-example/Banner.jpg
---

Just before we went into quarantine, I was designing clothes to be shown in a fashion show run by the USC Fashion Industry Association. We planned the theme for the fashion show to be black-and-white so we could incorporate several looks from the members of the club. We were fortunate to work with both photographers from the photography club and aspiring models who were also students at USC. Here are some of the looks I created!

<!-- Slideshow container -->
<div class="slideshow-container">

  <!-- Full-width images with number and caption text -->
  <div class="mySlides fade">
    <div class="numbertext">1 / 6</div>
    <img src="{{ "/assets/img/content/bw/bw1-min.jpg" | absolute_url }}" style="width:100%">
    <!-- <div class="text">Caption Text</div> -->
  </div>

  <div class="mySlides fade">
    <div class="numbertext">2 / 6</div>
    <img src="{{ "/assets/img/content/bw/bw2-min.jpg" | absolute_url }}" style="width:100%">
    <!-- <div class="text">Caption Text</div> -->
  </div>

  <div class="mySlides fade">
    <div class="numbertext">3 / 6</div>
    <img src="{{ "/assets/img/content/bw/bw3-min.jpg" | absolute_url }}" style="width:100%">
    <!-- <div class="text">Caption Text</div> -->
  </div>

  <div class="mySlides fade">
    <div class="numbertext">4 / 6</div>
    <img src="{{ "/assets/img/content/bw/bw4-min.jpg" | absolute_url }}" style="width:100%">
    <!-- <div class="text">Caption Text</div> -->
  </div>

  <div class="mySlides fade">
    <div class="numbertext">5 / 6</div>
    <img src="{{ "/assets/img/content/bw/bw5-min.jpg" | absolute_url }}" style="width:100%">
    <!-- <div class="text">Caption Text</div> -->
  </div>

  <div class="mySlides fade">
    <div class="numbertext">6 / 6</div>
    <img src="{{ "/assets/img/content/bw/bw6-min.jpg" | absolute_url }}" style="width:100%">
    <!-- <div class="text">Caption Text</div> -->
  </div>

  <!-- Next and previous buttons -->
  <a class="prev" onclick="plusSlides(-1)">&#10094;</a>
  <a class="next" onclick="plusSlides(1)">&#10095;</a>
</div>
<br>

<!-- The dots/circles -->
<div style="text-align:center">
  <span class="dot" onclick="currentSlide(1)"></span>
  <span class="dot" onclick="currentSlide(2)"></span>
  <span class="dot" onclick="currentSlide(3)"></span>
  <span class="dot" onclick="currentSlide(4)"></span>
  <span class="dot" onclick="currentSlide(5)"></span>
  <span class="dot" onclick="currentSlide(6)"></span>
</div>

<script>
  var slideIndex = 1;
showSlides(slideIndex);

// Next/previous controls
function plusSlides(n) {
  showSlides(slideIndex += n);
}

// Thumbnail image controls
function currentSlide(n) {
  showSlides(slideIndex = n);
}

function showSlides(n) {
  var i;
  var slides = document.getElementsByClassName("mySlides");
  var dots = document.getElementsByClassName("dot");
  if (n > slides.length) {slideIndex = 1}
  if (n < 1) {slideIndex = slides.length}
  for (i = 0; i < slides.length; i++) {
      slides[i].style.display = "none";
  }
  for (i = 0; i < dots.length; i++) {
      dots[i].className = dots[i].className.replace(" active", "");
  }
  slides[slideIndex-1].style.display = "block";
  dots[slideIndex-1].className += " active";
}
</script>

<link rel="stylesheet" href="{{ "/assets/css/slideshow.css" | absolute_url }}"/>