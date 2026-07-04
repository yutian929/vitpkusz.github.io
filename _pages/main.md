---
layout: page
permalink: /
title: Lab
description:

carousel_autoplay_delay: 3500

highlighted_projects:
  - teaser_img: /assets/img/vit-pkusz/dap.png
    caption:
    title: "DAP: Doppler-aware Point Network for Heterogeneous mmWave Action Recognition"
    link: /publications/
---

<style>
  .header-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 2rem;
    margin-top: 1rem;
  }

  .logo-container {
    display: flex;
    align-items: center;
    gap: 1rem;
  }

  .logo-container img {
    height: 72px;
    width: auto;
    object-fit: contain;
  }

  .lab-title {
    font-size: 2rem;
    font-weight: bold;
    color: var(--global-text-color);
    text-align: right;
  }

  @media (max-width: 576px) {
    .header-container {
      align-items: flex-start;
      flex-direction: column;
      gap: 1rem;
    }

    .lab-title {
      text-align: left;
    }
  }
</style>

<div class="header-container">
  <div class="logo-container">
    <img src="{{ '/assets/img/vit-pkusz/logo.png' | relative_url }}" alt="Visual Intelligence Team logo">
  </div>
  <div class="lab-title">Visual Intelligence Team</div>
</div>

<!-- ============================================ -->
<div class="clearfix"></div>
<!-- ============================================ -->

<!-- ============================================ -->
<!-- Swiper CSS -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.css">

<!-- Swiper Styles -->
<style>
  .swiper {
    width: 100%;
    height: 500px;
    margin-bottom: 2rem;
  }

  .swiper-slide {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background: var(--global-card-bg-color);
    text-align: center;
    font-size: 18px;
  }

  .swiper-button-next::after,
  .swiper-button-prev::after {
    color: var(--global-theme-color);
    font-size: 24px;
  }

  .swiper-pagination-bullet-active {
    background: var(--global-theme-color);
  }

  .swiper-slide video,
  .swiper-slide img {
    width: 100%;
    height: 100%;
    max-height: 400px;
    object-fit: contain;
    border-radius: 12px;
    background: #fff;
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.15);
    overflow: hidden;
  }

  .slide-title {
    margin-top: 0.5rem;
    font-weight: bold;
    font-size: 1.1rem;
    color: var(--global-text-color);
  }
</style>

<!-- Swiper Markup -->
<div class="swiper mySwiper">
  <div class="swiper-wrapper">
    {% for item in page.highlighted_projects %}
      <div class="swiper-slide">
        {% if item.link %}
          <a href="{{ item.link | relative_url }}" style="text-decoration: none; color: inherit;">
        {% endif %}

        {% if item.teaser_video %}
          <video src="{{ item.teaser_video | relative_url }}" autoplay muted loop playsinline poster="{{ item.teaser_img | relative_url }}"></video>
        {% elsif item.teaser_img %}
          <img src="{{ item.teaser_img | relative_url }}" alt="{{ item.title }}">
        {% endif %}

        {% if item.title %}
          <div class="slide-title">{{ item.title }}</div>
        {% endif %}

        {% if item.link %}
          </a>
        {% endif %}
      </div>
    {% endfor %}
  </div>

  <div class="swiper-button-next"></div>
  <div class="swiper-button-prev"></div>
  <div class="swiper-pagination"></div>
</div>

<!-- Swiper JS -->
<script src="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.js"></script>

<!-- Swiper Initialization -->
<script>
  var swiper = new Swiper(".mySwiper", {
    spaceBetween: 30,
    centeredSlides: true,
    loop: false,
    watchSlidesProgress: true,
    speed: 1000,
    effect: "fade",
    fadeEffect: {
      crossFade: true,
    },
    autoplay: {
      delay: {{ page.carousel_autoplay_delay | default: 3500 }},
      disableOnInteraction: false,
      reverseDirection: false,
      stopOnLastSlide: false,
    },
    pagination: {
      el: ".swiper-pagination",
      clickable: true,
      dynamicBullets: false,
      type: "bullets",
    },
    navigation: {
      nextEl: ".swiper-button-next",
      prevEl: ".swiper-button-prev",
    },
    on: {
      slideChangeTransitionStart: function () {
        const activeSlide = this.slides[this.activeIndex];
        const activeVideo = activeSlide.querySelector("video");
        if (activeVideo) {
          activeVideo.currentTime = 0;
          activeVideo.play();
        }
      },
      slideChangeTransitionEnd: function () {
        const videos = document.querySelectorAll(".swiper-slide video");
        videos.forEach((video, index) => {
          if (index !== this.activeIndex) {
            video.pause();
            video.currentTime = 0;
          }
        });
      },
      init: function () {
        const firstVideo = this.slides[0].querySelector("video");
        if (firstVideo) {
          firstVideo.currentTime = 0;
          firstVideo.play();
        }
      },
      reachEnd: function () {
        setTimeout(() => {
          this.slideTo(0);
        }, {{ page.carousel_autoplay_delay | default: 3500 }});
      },
    },
  });
</script>

<!-- ============================================ -->
<!-- News -->
<h2>News</h2>
{% include news.liquid %}
<!-- ============================================ -->

{% include recent_publications.liquid %}
