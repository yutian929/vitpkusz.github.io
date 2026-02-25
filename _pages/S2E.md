---
layout: research
permalink: /S2E/
title: "S2E"
page_title: "From Seeing to Experiencing: Scaling Navigation Foundation Models with Reinforcement Learning"
description: "<h3>ICLR 2026</h3>"

authors:

- {name: "Honglin He*", url: "https://dhlinv.github.io/", institution: "1"}
- {name: "Yukai Ma*", url: "https://yukai-ma.github.io/", institution: "1"}
- {name: "Brad Squicciarini", url: "https://www.linkedin.com/in/brad-squicciarini-478954126/", institution: "2"}
- {name: "Wayne Wu", url: "https://wywu.github.io/", institution: "1"}
- {name: "Bolei Zhou", url: "https://boleizhou.github.io/", institution: "1"}

institutions:

- {name: "University of California, Los Angeles", institution: "1"}
- {name: "Coco Robotics", institution: "2"}

nav: false
nav_order: 1
code_link: https://github.com/VAIL-UCLA/S2E
pdf_link: https://arxiv.org/abs/2507.22028

---

<div class="embed-responsive embed-responsive-16by9">
  <video muted autoplay playsinline controls loop style="position: absolute; top: 0%; left: 0%; width: 100%; height: 100%;">
        <source src="../assets/projects/s2e/teaser_web.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video>
</div>

<div class="research-section">
    <h3 style="text-align: center">TL;DR</h3>
    <ul style="list-style-type: none; padding-left: 0;">
      <strong>S2E</strong> is a <em>unified</em> learning framework that scales navigation foundation models from passive offline video to interactive decision-making through reinforcement learning.<br><br>
    1. 📦 Provides a general framework for learning navigation from both offline data and online interaction.<br>
    2. 🔌 Introduces a plug-and-play <strong>Residual-Attention Module</strong> for efficient adaptation and scaling in RL.<br>
    3. 🧭 Releases <strong>NavBench-GS</strong>, a realistic 3D Gaussian Splatting benchmark for evaluating navigation performance in closed-loop, interactive, and physically grounded environments.
  </ul>
</div>

<!--research-section-splitter-->

## S2E Model architecture

<div class="img-container" style="width: 100%; margin: 0 auto;">
    <img src="../assets/projects/s2e/s2e_model.png" class="my-image" alt="Image" />
</div>
 
S2E pipeline consists of two key components:<br>
(1) Anchor-Guided Distribution Matching: A framework that uses anchor-conditioned architecture to learn multi-modal trajectory distributions from offline real-world videos, improving model capability from the side of representation.<br>
(2) Residual Attention Module: A lightweight residual design that fine-tunes pretrained attention blocks via reinforcement learning in simulation, enabling new behaviors (e.g., obstacle avoidance) while preserving general visual-motor priors.

<!--research-section-splitter-->

## Environments for Pretraining and Finetuning

### Video-Action Pretraining

<div class="embed-responsive embed-responsive-16by9">
  <video muted autoplay playsinline controls loop style="position: absolute; top: 0%; left: 0%; width: 100%; height: 100%;">
        <source src="../assets/projects/s2e/pretrain_web.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video>
</div>

### URBAN-SIM Closed-loop Finetuning

<div class="embed-responsive embed-responsive-16by9">
  <video muted autoplay playsinline controls loop style="position: absolute; top: 0%; left: 0%; width: 100%; height: 100%;">
        <source src="../assets/projects/s2e/finetune_web.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video>
</div>

<!--research-section-splitter-->

## NavBench-GS: Closed-Loop 3DGS Navigation Benchmark

<div class="embed-responsive embed-responsive-16by9">
  <video muted autoplay playsinline controls loop style="position: absolute; top: 0%; left: 0%; width: 100%; height: 100%;">
        <source src="../assets/projects/s2e/navbench_gs.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video>
</div>

We build NavBench-GS, a 3D Gaussian Splatting-based benchmark for evaluating navigation policies in closed-loop, visually reconstructed urban environments with simulated objects and pedestrians.


<!--research-section-splitter-->
## Real-World Deployment

### Obstacle Avoidance

<div class="embed-responsive embed-responsive-16by9">
  <video muted autoplay playsinline controls loop style="position: absolute; top: 0%; left: 0%; width: 100%; height: 100%;">
        <source src="../assets/projects/s2e/coco_obstacle.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video>
</div>

### Cross-Embodiment

<div class="embed-responsive embed-responsive-16by9">
  <video muted autoplay playsinline controls loop style="position: absolute; top: 0%; left: 0%; width: 100%; height: 100%;">
        <source src="../assets/projects/s2e/obstacles.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video>
</div>

<div class="embed-responsive embed-responsive-16by9">
  <video muted autoplay playsinline controls loop style="position: absolute; top: 0%; left: 0%; width: 100%; height: 100%;">
        <source src="../assets/projects/s2e/obstacles2_web.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video>
</div>

### Comparison

<div class="embed-responsive embed-responsive-16by9">
  <video muted autoplay playsinline controls loop style="position: absolute; top: 0%; left: 0%; width: 100%; height: 100%;">
        <source src="../assets/projects/s2e/comparisons.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video>
</div>

### Long-Horizon Navigation

<div class="embed-responsive embed-responsive-16by9">
  <video muted autoplay playsinline controls loop style="position: absolute; top: 0%; left: 0%; width: 100%; height: 100%;">
        <source src="../assets/projects/s2e/longnav_web.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video>
</div>

<!--research-section-splitter-->

## Reference

```
@article{he2026seeing,
    title={From Seeing to Experiencing: Scaling Navigation Foundation Models with Reinforcement Learning},
    author={He, Honglin and Ma, Yukai and Squicciarini, Brad and Wu, Wayne and Zhou, Bolei},
    journal={The Fourteenth International Conference on Learning Representations},
    year={2026}
}
```

