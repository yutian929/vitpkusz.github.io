---
layout: page
permalink: /publications/
title: Publications
nav: true
nav_order: 2
description:
---

<style>
  .publications h2.year,
  .publications h2,
  .publications h3.year,
  .publications h3 {
    color: var(--global-theme-color) !important;
    font-weight: 600 !important;
    font-size: 2rem !important;
    margin-top: 0 !important;
    margin-bottom: 0 !important;
  }

  .publication-tags-container {
    margin-bottom: 1rem;
  }

  .tag-buttons {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
  }

  .tag-btn {
    border: 1px solid var(--global-divider-color);
    border-radius: 6px;
    background: var(--global-card-bg-color);
    color: var(--global-text-color);
    padding: 0.35rem 0.7rem;
    line-height: 1.2;
  }

  .tag-btn.active {
    border-color: var(--global-theme-color);
    color: var(--global-theme-color);
  }
</style>

Selected publications from the Visual Intelligence Team.

<div class="publication-tags-container">
  <div class="tag-buttons">
    <button class="tag-btn active" data-tag="all">All</button>
    <button class="tag-btn" data-tag="Computer Vision">Computer Vision</button>
    <button class="tag-btn" data-tag="Signal Processing">Signal Processing</button>
    <button class="tag-btn" data-tag="Action Recognition">Action Recognition</button>
    <button class="tag-btn" data-tag="Others">Others</button>
  </div>
</div>

<div class="publications">
  {% bibliography %}
</div>

<script>
  document.addEventListener("DOMContentLoaded", function () {
    const tagButtons = document.querySelectorAll(".tag-btn");
    const publications = document.querySelectorAll(".publications ol.bibliography li");

    tagButtons.forEach((button) => {
      button.addEventListener("click", function () {
        tagButtons.forEach((btn) => btn.classList.remove("active"));
        this.classList.add("active");

        const selectedTag = this.getAttribute("data-tag");

        publications.forEach((publication) => {
          const publicationDiv = publication.querySelector("div[data-tags]");
          if (selectedTag === "all") {
            publication.style.display = "block";
            return;
          }

          const tags = publicationDiv ? publicationDiv.getAttribute("data-tags") || "" : "";
          publication.style.display = tags.toLowerCase().includes(selectedTag.toLowerCase()) ? "block" : "none";
        });
      });
    });
  });
</script>
