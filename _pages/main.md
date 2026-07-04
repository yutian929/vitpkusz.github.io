---
layout: page
permalink: /
title: Home
description: Visual Intelligence Team, HRI Lab, PKU Shenzhen
_styles: >
  .vit-home {
    --vit-accent: #a50f1c;
    --vit-accent-soft: rgba(165, 15, 28, 0.08);
  }

  .vit-hero {
    display: grid;
    grid-template-columns: minmax(88px, 120px) minmax(0, 1fr);
    gap: 1.25rem;
    align-items: center;
    padding: 1.25rem 0 1.75rem;
    border-bottom: 1px solid var(--global-divider-color);
  }

  .vit-logo {
    width: 112px;
    height: 112px;
    object-fit: contain;
  }

  .vit-eyebrow {
    margin: 0 0 0.35rem;
    color: var(--vit-accent);
    font-size: 0.92rem;
    font-weight: 700;
    letter-spacing: 0;
  }

  .vit-title {
    margin: 0;
    color: var(--global-text-color);
    font-size: clamp(2rem, 5vw, 3.25rem);
    font-weight: 800;
    line-height: 1.05;
  }

  .vit-subtitle {
    margin: 0.65rem 0 0;
    color: var(--global-text-color-light);
    font-size: 1.05rem;
  }

  .vit-section {
    margin-top: 2.4rem;
  }

  .vit-section h2 {
    margin: 0 0 1rem;
    color: var(--global-text-color);
    font-size: 1.45rem;
    font-weight: 750;
  }

  .vit-panel {
    padding: 1.1rem 1.2rem;
    border: 1px solid var(--global-divider-color);
    border-radius: 8px;
    background: var(--global-card-bg-color);
  }

  .vit-news-list,
  .vit-award-list,
  .vit-name-list {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  .vit-news-list li + li,
  .vit-award-list li + li,
  .vit-name-list li + li {
    margin-top: 0.85rem;
  }

  .vit-date {
    display: block;
    color: var(--vit-accent);
    font-weight: 700;
  }

  .vit-paper {
    display: grid;
    grid-template-columns: minmax(0, 1fr) minmax(260px, 42%);
    gap: 1.25rem;
    align-items: center;
  }

  .vit-paper h3,
  .vit-team-group h3 {
    margin: 0 0 0.55rem;
    color: var(--global-text-color);
    font-size: 1.08rem;
    font-weight: 750;
    line-height: 1.3;
  }

  .vit-paper p {
    margin: 0.45rem 0 0;
  }

  .vit-venue {
    color: var(--global-text-color-light);
  }

  .vit-paper img {
    width: 100%;
    aspect-ratio: 595 / 333;
    object-fit: contain;
    border: 1px solid var(--global-divider-color);
    border-radius: 8px;
    background: #fff;
  }

  .vit-award-list li {
    padding-left: 0.9rem;
    border-left: 3px solid var(--vit-accent);
  }

  .vit-team-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 1rem;
  }

  .vit-team-group {
    padding: 1rem;
    border: 1px solid var(--global-divider-color);
    border-radius: 8px;
    background: var(--global-card-bg-color);
  }

  .vit-team-lead {
    grid-column: 1 / -1;
  }

  .vit-person {
    display: grid;
    grid-template-columns: 128px minmax(0, 1fr);
    gap: 1rem;
    align-items: center;
  }

  .vit-person img {
    width: 128px;
    height: 128px;
    object-fit: cover;
    border-radius: 8px;
    border: 1px solid var(--global-divider-color);
  }

  .vit-person strong,
  .vit-name-list li {
    color: var(--global-text-color);
    font-weight: 650;
  }

  html[data-theme='dark'] .vit-paper img {
    background: #f8f8f8;
  }

  @media (max-width: 720px) {
    .vit-hero,
    .vit-paper,
    .vit-team-grid,
    .vit-person {
      grid-template-columns: 1fr;
    }

    .vit-logo,
    .vit-person img {
      width: 112px;
      height: 112px;
    }

    .vit-paper img {
      max-width: 100%;
    }
  }
---

<div class="vit-home">
  <section class="vit-hero" aria-label="Visual Intelligence Team">
    <img class="vit-logo" src="{{ '/assets/img/vit-pkusz/logo.png' | relative_url }}" alt="Visual Intelligence Team logo">
    <div>
      <p class="vit-eyebrow">HRI Lab | PKU Shenzhen</p>
      <h1 class="vit-title">Visual Intelligence Team</h1>
      <p class="vit-subtitle">Visual Intelligence Team, HRI Lab, PKU Shenzhen</p>
    </div>
  </section>

  <section class="vit-section" aria-labelledby="vit-news">
    <h2 id="vit-news">News</h2>
    <div class="vit-panel">
      <ul class="vit-news-list">
        <li>
          <span class="vit-date">June 30, 2026</span>
          Four students earned their Master's degrees. Congratulations to Jiajie Liu, Jinyan Zhang, Jingting Liu, Di Wang!
        </li>
        <li>
          <span class="vit-date">June 18, 2026</span>
          Two papers are accepted to ECCV 2026. Congratulations to Ziyi Wang, Jiaying Lin!
        </li>
      </ul>
    </div>
  </section>

  <section class="vit-section" aria-labelledby="vit-papers">
    <h2 id="vit-papers">Recent Papers</h2>
    <div class="vit-panel vit-paper">
      <div>
        <h3>DAP: Doppler-aware Point Network for Heterogeneous mmWave Action Recognition</h3>
        <p>Jiaying Lin, Shiman Wu, Jinfu Liu, Can Wang, Mengyuan Liu</p>
        <p class="vit-venue">European Conference on Computer Vision (ECCV), 2026</p>
      </div>
      <img src="{{ '/assets/img/vit-pkusz/dap.png' | relative_url }}" alt="DAP dataset and protocol overview">
    </div>
  </section>

  <section class="vit-section" aria-labelledby="vit-awards">
    <h2 id="vit-awards">Awards</h2>
    <div class="vit-panel">
      <ul class="vit-award-list">
        <li>Jiajie Liu: Peking University Outstanding Graduate, 2026</li>
        <li>Peiming Li: Peking University National Scholarship, 2025</li>
        <li>Peiming Li: Peking University BYD Scholarship, 2025</li>
        <li>Ziyi Wang: Peking University Luo Yuehua Scholarship, 2025</li>
        <li>Ziyi Wang: Peking University Merit Student, 2025</li>
        <li>Jiajie Liu: Peking University Outstanding Research Award, 2025</li>
        <li>Jinyan Zhang: Peking University Merit Student, 2024</li>
      </ul>
    </div>
  </section>

  <section class="vit-section" aria-labelledby="vit-team">
    <h2 id="vit-team">Team</h2>
    <div class="vit-team-grid">
      <section class="vit-team-group vit-team-lead">
        <h3>Principal Investigator</h3>
        <div class="vit-person">
          <img src="{{ '/assets/img/vit-pkusz/mengyuan-liu.png' | relative_url }}" alt="Mengyuan Liu">
          <strong>Mengyuan Liu</strong>
        </div>
      </section>

      <section class="vit-team-group">
        <h3>Postdoctoral Researchers</h3>
        <ul class="vit-name-list">
          <li>Yuxuan Li</li>
        </ul>
      </section>

      <section class="vit-team-group">
        <h3>Ph.D. Students</h3>
        <ul class="vit-name-list">
          <li>Xinshun Wang</li>
          <li>Juyi Sheng</li>
        </ul>
      </section>

      <section class="vit-team-group">
        <h3>M.S. Students</h3>
        <ul class="vit-name-list">
          <li>Ziyi Wang</li>
          <li>Peiming Li</li>
          <li>Yangting Lin</li>
          <li>Yutian Zhang</li>
          <li>Jiaying Lin</li>
          <li>Jianian Gong</li>
          <li>Tianming Xu</li>
          <li>Jiayu Zhang</li>
          <li>Jincheng Li</li>
          <li>Jiale Li</li>
          <li>Zhicheng Liao</li>
          <li>Mingjie Zhang</li>
        </ul>
      </section>

      <section class="vit-team-group">
        <h3>Visiting Students and Scholars</h3>
        <ul class="vit-name-list">
          <li>Wanying Zhang</li>
          <li>Zhongbing Fang</li>
          <li>Jinfu Liu</li>
          <li>Zhichao Deng</li>
          <li>Yuhang Wen</li>
          <li>Zixuan Tang</li>
          <li>Shidan He</li>
          <li>Yang Liu</li>
          <li>Zongying Li</li>
          <li>Haoqiang Wang</li>
          <li>Qianshuo Hu</li>
          <li>Xin Du</li>
          <li>Sheng Yan</li>
          <li>Hongchang Jin</li>
          <li>Yi Wang</li>
          <li>Kefan Chen</li>
          <li>Chao Yuan</li>
          <li>Yulei Yang</li>
        </ul>
      </section>

      <section class="vit-team-group">
        <h3>Alumni</h3>
        <ul class="vit-name-list">
          <li>Jiajie Liu</li>
          <li>Jinyan Zhang</li>
          <li>Jingting Liu</li>
          <li>Di Wang</li>
        </ul>
      </section>
    </div>
  </section>
</div>
