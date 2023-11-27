---
layout: post
title:  "2021 LA Live Skating Show"
date:   2021-12-09 08:00:00
blurb: "The projects I did in Quarantine"
og_image: /assets/img/content/post-example/Banner.jpg
---

LA Live is our annual skating show. This year I choreographed a pairs skating program to the song "Snowman" by Sia with my friend <a href="https://www.lillianzeng.com/about">Lillian Zeng</a>.

<iframe width="100%" height="315" src="https://www.youtube.com/embed/UqVspCbZ7H0?si=PFfCEqjTAyIWY3eo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

<br>
We did the show with the entire skating club as our end-of-semester event. If you are in LA in December, come check it out. The performance is on the opening day of the skating rink!

<!-- Slideshow container -->
<div class="slideshow-container" style="width:60%;">

  <!-- Full-width images with number and caption text -->
  <div class="mySlides fade">
    <div class="numbertext">1 / 3</div>
    <img src="{{ "/assets/img/content/lalive/7T3B8650.JPG" | absolute_url }}" style="width:100%">

  </div>

  <div class="mySlides fade">
    <div class="numbertext">2 / 3</div>
    <img src="{{ "/assets/img/content/lalive/7T3B8659.JPG" | absolute_url }}" style="width:100%">
  </div>

  <div class="mySlides fade">
    <div class="numbertext">3 / 3</div>
    <img src="{{ "/assets/img/content/lalive/IMG_3250.JPG" | absolute_url }}" style="width:100%">
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