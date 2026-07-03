---
layout: research
permalink: /micromobility_workshop/
title: Workshop on Foundation Models for Micromobility
page_title: 
description: 
nav: false
nav_order: 1
---




<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js" integrity="sha384-MrcW6ZMFYlzcLA8Nl+NtUVF0sA7MsXsP1UyJoMp4YLEuNSfAP+JcXn/tWtIaxVXM" crossorigin="anonymous"></script>


<style>
.title {
    color: #414446;
    clear: both;
    text-align: center;
}

.title-main {
    font-size: 30pt; /* Adjust main title size */
}

.title-sub {
    font-size: 18pt; /* Adjust subtitle size */
}

.time, .location {
    font-size: 12pt; /* Adjust time and location font size */
}

.logo {
    width: 100%;
    padding: 2px 2px 2px 2px;
    margin: 0px 0px 1px 0px;
    object-fit: contain;
}

.caption {
    padding: 3px 0px 3px 0px;
    margin: 0px 0px 3px 0px;
    text-align: center;
    font-size: 14pt;
}
.caption span {
    font-size: 10pt;
}
.caption a:hover {text-decoration:none;}

.carousel-item {
    text-align: center;
}
.carousel-caption {
    background: rgba(230, 230, 230, 0.9);
}

.thumbnail {
    padding: 2px 2px 2px 2px;
    margin: 0px 0px 1px 0px;
}

.thumbnail img {
    width: 100%;
    aspect-ratio: 1 / 1;
    object-fit: cover;
}
@media (min-width: 576px) {
    .thumbnail img {
        object-fit: cover;
    }
    .thumbnail img.top-left {
        object-position: 0px 0px;
    }
}
 

.thumbnail ul {
    display: block;
    list-style-type: none;
    margin: 0px;
    padding: 5px;
    text-align: center;
}
@media (hover: hover) {
    .thumbnail div {
        position: relative;
        overflow: hidden;
    }
    .thumbnail ul {
        background: rgba(200, 200, 200, 0.7);
        position: absolute;
        bottom: -100%;
        left: 0px;
        right: 0px;
        transition: bottom 0.2s ease-in-out;
    }
    .thumbnail:hover ul {
        bottom: 0px;
    }
}

/* Dark mode overrides */
html[data-theme='dark'] .title {
    color: #e0e0e0 !important;
}

html[data-theme='dark'] .title h2,
html[data-theme='dark'] .title h5 {
    color: #e0e0e0 !important;
}

html[data-theme='dark'] .caption {
    color: #e0e0e0 !important;
}

html[data-theme='dark'] .caption span {
    color: #b0b0b0 !important;
}

html[data-theme='dark'] .carousel-caption {
    background: rgba(40, 40, 40, 0.9) !important;
}

html[data-theme='dark'] .thumbnail ul {
    background: rgba(50, 50, 50, 0.8) !important;
}

html[data-theme='dark'] .thumbnail ul .icon i {
    color: #e0e0e0 !important;
}

html[data-theme='dark'] .container h2,
html[data-theme='dark'] .container h3,
html[data-theme='dark'] .container h5 {
    color: #e0e0e0 !important;
}

html[data-theme='dark'] .container p,
html[data-theme='dark'] .container div,
html[data-theme='dark'] .container td,
html[data-theme='dark'] .container th,
html[data-theme='dark'] .container li,
html[data-theme='dark'] .container b,
html[data-theme='dark'] .container span {
    color: #e0e0e0 !important;
}

html[data-theme='dark'] .container {
    color: #e0e0e0 !important;
}

html[data-theme='dark'] body,
html[data-theme='dark'] .post {
    background-color: #1a1a2e !important;
}

html[data-theme='dark'] .schedule-table th {
    background-color: var(--global-theme-color, #2698BA) !important;
    color: #fff !important;
}

html[data-theme='dark'] .schedule-table td {
    border-bottom-color: #444 !important;
    color: #e0e0e0 !important;
}

html[data-theme='dark'] .schedule-table tr:nth-child(even) {
    background-color: rgba(255, 255, 255, 0.05) !important;
}

html[data-theme='dark'] .schedule-table tr:hover {
    background-color: rgba(255, 255, 255, 0.08) !important;
}

html[data-theme='dark'] .schedule-table .break-row {
    background-color: rgba(255, 255, 255, 0.07) !important;
}

html[data-theme='dark'] a {
    color: var(--global-theme-color, #2698BA) !important;
}

html[data-theme='dark'] .col-md-7,
html[data-theme='dark'] .col-md-5 {
    color: #e0e0e0 !important;
}

</style>

<div class="title">
                <h2 class="title-main">Workshop on Foundation Models for Micromobility</h2>
                <h5 class="title-sub ">RSS 2026 Workshop, Sydney, Australia</h5>
                <h5 class="time">Time: TBD, Location: TBD</h5>
</div>

 
## 👋 Introduction


<div class="row align-items-center">
  <div class="col-md-5">
    <img src="{{ '/assets/img/micromobility_workshop/teaser.png' | relative_url }}" class="my-image" alt="Image" style="width: 100%;" />
  </div>
  <div class="col-md-7">
    With the rapid development of Embodied AI technologies, a wide variety of mobile robots are starting to share the streets and sidewalks with pedestrians. While researchers have made significant progress in mobility, especially in autonomous driving, micromobility remains comparatively under-studied. Despite their potential, sidewalks present a much more complex and unpredictable environment for mobility than typical roads and streets. Broken curbs, uneven pavements, and narrow streets often make the terrain challenging for passage, while crowds of dense pedestrians make safe and efficient mobility even more difficult.
    <br><br>
    <b>Workshop on Foundation Models for Micromobility</b> aims to bring together the growing community of researchers and practitioners at the intersection of computer vision, robotics, simulation, and machine learning, with a particular focus on how foundation models can enable robust, generalizable, and scalable sidewalk micromobility. The workshop will serve as a forum to discuss the latest advances, open problems, emerging datasets and benchmarks related to sidewalk micromobility. We expect participation from sub-communities including: (i) foundation models, (ii) robot learning, (iii) computer vision, (iv) navigation, and (v) simulation.
  </div>
</div>
---

## 📅 Schedule
The workshop will take place on **TBD**, at **TBD**.  
<style>
  .schedule-table {
    width: 100%;
    border-collapse: collapse;
    margin: 1.5rem 0;
  }
  .schedule-table th {
    background-color: var(--global-theme-color, #2698BA);
    color: #fff;
    padding: 0.75rem 1rem;
    text-align: left;
    font-weight: 600;
  }
  .schedule-table td {
    padding: 0.75rem 1rem;
    border-bottom: 1px solid #e0e0e0;
    vertical-align: top;
  }
  .schedule-table tr:nth-child(even) {
    background-color: rgba(0, 0, 0, 0.03);
  }
  .schedule-table tr:hover {
    background-color: rgba(0, 0, 0, 0.06);
  }
  .schedule-table .time-col {
    white-space: nowrap;
    font-weight: 500;
    width: 240px;
  }
  .schedule-table .break-row {
    background-color: rgba(0, 0, 0, 0.05);
    font-style: italic;
  }
  html[data-theme='dark'] .schedule-table td {
    border-bottom-color: #444;
  }
  html[data-theme='dark'] .schedule-table tr:nth-child(even) {
    background-color: rgba(255, 255, 255, 0.05);
  }
  html[data-theme='dark'] .schedule-table tr:hover {
    background-color: rgba(255, 255, 255, 0.08);
  }
  html[data-theme='dark'] .schedule-table .break-row {
    background-color: rgba(255, 255, 255, 0.07);
  }
</style>

**Tentative Schedule**

<table class="schedule-table">
  <thead>
    <tr>
      <th>Time</th>
      <th>Event</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td class="time-col">08:55 am – 09:00 am</td>
      <td>Welcome and Introduction</td>
    </tr>
    <tr>
      <td class="time-col">09:00 am – 09:35 am</td>
      <td>Keynote Talk 1 — Dinesh Manocha (Confirmed)</td>
    </tr>
    <tr>
      <td class="time-col">09:35 am – 09:55 am</td>
      <td>Spotlight Presentations I (4 mins × 5 accepted abstracts)</td>
    </tr>
    <tr class="break-row">
      <td class="time-col">09:55 am – 10:25 am</td>
      <td>☕ Coffee Break</td>
    </tr>
    <tr>
      <td class="time-col">10:25 am – 10:55 am</td>
      <td>Sidewalk Micromobility Navigation Challenge Session</td>
    </tr>
    <tr>
      <td class="time-col">10:55 am – 11:30 am</td>
      <td>Keynote Talk 2 — Joydeep Biswas (Confirmed)</td>
    </tr>
    <tr>
      <td class="time-col">11:30 am – 11:50 am</td>
      <td>Spotlight Presentations II (4 mins × 5 accepted abstracts)</td>
    </tr>
    <tr>
      <td class="time-col">11:50 am – 12:35 pm</td>
      <td>Panel Discussion — "How to solve sidewalk autonomy"</td>
    </tr>
    <tr>
      <td class="time-col">12:35 pm – 12:55 pm</td>
      <td>Open Discussion and Community Wrap-up</td>
    </tr>
  </tbody>
</table>

 

---

## 🎤 Speakers

<div class="row justify-content-center">
    <div class="col-xs-6 col-md-3">
        <div class="thumbnail">
            <div>
                <img src="{{ '/assets/img/micromobility_workshop/dinesh.jpg' | relative_url }}" alt="Dinesh Monacha">
                <ul class="social">
                    <a href="https://www.cs.umd.edu/people/dmanocha">
                        <li class="icon"><i class="fa fa-home"></i></li>
                    </a>
                </ul>
            </div>
            <div class="caption">
                Dinesh Monacha<br><span>University of Maryland, College Park</span>
            </div>
        </div>
    </div>
    <div class="col-xs-6 col-md-3">
        <div class="thumbnail">
            <div>
                <img src="{{ '/assets/img/micromobility_workshop/joydeep.jpg' | relative_url }}" alt="Joydeep Biswas">
                <ul class="social">
                    <a href="https://www.joydeepb.com/">
                        <li class="icon"><i class="fa fa-home"></i></li>
                    </a>
                </ul>
            </div>
            <div class="caption">
                Joydeep Biswas<br><span>University of Texas at Austin</span>
            </div>
        </div>
    </div>
</div>
  

---

## 📋 Organizers
<div class="row justify-content-center">
    <div class="col-xs-6 col-md-3">
        <div class="thumbnail">
            <div>
                <img src="{{ '/assets/team/honglinhe.jpg' | relative_url }}" alt="Honglin He">
                <ul class="social">
                    <a href="https://dhlinv.github.io/">
                        <li class="icon"><i class="fa fa-home"></i></li>
                    </a>
                </ul>
            </div>
            <div class="caption">
                Honglin He<br><span>University of California, Los Angeles</span>
            </div>
        </div>
    </div>
    <div class="col-xs-6 col-md-3">
        <div class="thumbnail">
            <div>
                <img src="{{ '/assets/img/micromobility_workshop/mingxuan.png' | relative_url }}" alt="Mingxuan Liu">
                <ul class="social">
                    <a href="https://oatmealliu.github.io/">
                        <li class="icon"><i class="fa fa-home"></i></li>
                    </a>
                </ul>
            </div>
            <div class="caption">
                Mingxuan Liu<br><span>University of Trento</span>
            </div>
        </div>
    </div>
    <div class="col-xs-6 col-md-3">
        <div class="thumbnail">
            <div>
                <img src="{{ '/assets/img/micromobility_workshop/zhizheng.png' | relative_url }}" alt="Zhizheng Liu">
                <ul class="social">
                    <a href="https://bosmallear.github.io/">
                        <li class="icon"><i class="fa fa-home"></i></li>
                    </a>
                </ul>
            </div>
            <div class="caption">
                Zhizheng Liu<br><span>University of California, Los Angeles</span>
            </div>
        </div>
    </div>
</div>

<div class="row justify-content-center">
    <div class="col-xs-6 col-md-3">
        <div class="thumbnail">
            <div>
                <img src="{{ '/assets/img/micromobility_workshop/brad.avif' | relative_url }}" alt="Brad Squicciarini">
                <ul class="social">
                    <a href="https://www.linkedin.com/in/brad-squicciarini-478954126/">
                        <li class="icon"><i class="fa fa-home"></i></li>
                    </a>
                </ul>
            </div>
            <div class="caption">
                Brad Squicciarini<br><span>Coco Robotics</span>
            </div>
        </div>
    </div>
    <div class="col-xs-6 col-md-3">
        <div class="thumbnail">
            <div>
                <img src="{{ '/assets/team/bolei.jpg' | relative_url }}" alt="Bolei Zhou">
                <ul class="social">
                    <a href="https://boleizhou.github.io/">
                        <li class="icon"><i class="fa fa-home"></i></li>
                    </a>
                </ul>
            </div>
            <div class="caption">
                Bolei Zhou<br><span>University of California, Los Angeles</span>
            </div>
        </div>
    </div>
</div>
 
