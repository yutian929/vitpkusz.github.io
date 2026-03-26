---
layout: research
permalink: /BridgeSim/
title:  "BridgeSim: Unveiling the OL-CL Gap in End-to-End Autonomous Driving"
page_title: "BridgeSim: Unveiling the OL-CL Gap in End-to-End Autonomous Driving"
# authors:
#   - {name: "Zhenghao Peng", url: "https://pengzhenghao.github.io/"}
#   - {name: "Yuxin Liu",  url: "#"}
#   - {name: "Bolei Zhou",            url: "https://boleizhou.github.io/"}
institutions:
    - {name: "<p>University of California, Los Angeles</p>"}
    - {name: "<p>University of California, San Diego</p>"}
    - {name: "<p>Qualcomm</p>"}
nav: false
nav_order: 1
code_link: https://github.com/VAIL-UCLA/BridgeSim
# pdf_link: https://arxiv.org/pdf/2506.23316
---


<style>
.video-container {
  position: relative;
  max-width: 100%;
  margin: 0 auto 0;
}

.video-container video {
  display: block;
  margin: 0 auto;
  max-width: 100%;
  max-height: 100%;
}

.video-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 20px;
}
.video iframe {
    width: 100%;
    height: 250px;
}

@media (max-width: 600px) {
    .video-grid {
        grid-template-columns: 1fr;
    }
}
</style>

<div class="img-container" style="width: 80%; margin: auto auto;">
    <img src="../assets/projects/bridgesim/bridgesim.pdf" class="my-image" alt="Image" />
</div>


**BridgeSim** is a unified cross-simulator platform designed to evaluate OL pretrained E2E driving policies within high-fidelity CL environments in the MetaDrive simulator. BridgeSim designs a  Furthermore, BridgeSim offers a flexible deployment setting to simulate open-loop policy with varying execution frequencies and simulation horizons, providing the functional depth necessary for systematic and rigorous diagnosis of OL-CL gap. Consequently, BridgeSim bridges the critical divide between open-loop benchmarks limited to short-term static prediction and existing closed-loop frameworks that often lack the comprehensive functionality and annotations required for complex, reactive stress-testing.

&nbsp;
&nbsp;
:traffic_light: Unified structural framework on low-level control for policy transfer to maintain state-action compatibility across domains

&nbsp;
&nbsp;
:mag: Unified scenario protocol to incorporate diverse map scenarios (e.g., nuPlan, WOMD, and nuScenes) with heterogeneous traffic modes (e.g., log-replay, IDM and adversarial policies) to stress-test E2E driving policies under closed-loop simulation environment.

&nbsp;
&nbsp;
:rocket: Unified open-loop and closed-loop simulation modes and metrics for comprehensive evaluations.


<!--research-section-splitter-->


## Abstract

End-to-end autonomous driving has seen rapid progress on non-reactive simulation benchmarks such as NAVSIM, where planners are evaluated on PDMS-based metrics without environmental feedback. Yet gains on these open-loop (OL) metrics do not reliably transfer to closed-loop (CL) deployment, and the field continues to optimize for open-loop improvements. In this paper, we systematically decompose the root causes of this OL–CL deployment gap into two key factors: Information Asymmetry, resulting from observational domain shifts, and Objective Mismatch, driven by train-test optimization misalignment. Through principled analysis, we demonstrate that while Information Asymmetry is largely recoverable with standard adaptation, the primary catalyst for performance collapse is Objective Mismatch, specifically, biased Q-value estimates that fail to account for the reactive nature of the environment. We further show that under this mismatch, improving open-loop accuracy or scaling test-time computation over the open-loop objective yields diminishing or negative closed-loop returns. To this end, we propose a Test-Time Adaptation (TTA) framework that mitigates observational shift and debiases action-value estimates in inference time. Extensive experiments show that TTA effectively mitigates these biases and exhibits more favorable scaling dynamics than its baseline counterparts. Given these findings, we suggest the community reassess the prevailing reliance on non-reactive evaluation in driving research, and move toward closed-loop-aligned training and evaluation objectives that account for the interactive nature of real-world driving. 


<!--research-section-splitter-->


## Decomposing OL-CL Gap

<!-- <div class="img-container" style="width: 100%; margin: 0 auto;">
    <img src="../assets/projects/scenestreamer/framework.png" class="my-image" alt="Image" />
</div> -->

We define E2E policy as: 

<div>
$$\bar{\pi}^{d}_{\theta,\phi}(a,z,o \mid s) \triangleq \pi_{\phi}(a\mid z)\,P_\theta(z\mid o)\,\Omega^d(o\mid s)$$
</div>

The root causes of the OL-CL deployment gap are decomposed into two key factors:

- **Information Asymmetry** occurs when there exists an observational domain shift and the source policy receives collapsed partially observable states in the target simulator.

<div>
$$\Delta_{\mathrm{obs}}(\theta, \phi) \triangleq J(\pi^{\mathrm{source}}_{\theta,\phi}) - J(\pi^{\mathrm{target}}_{\theta,\phi})$$
</div>

- **Objective Mismatch** occurs when OL policies, which is optimized against OL proxy reward during the training time, encounters the CL objective that the learned Q-function gives deviated estimates of true state-action values.

<div>
$$\Delta_{\mathrm{obj}}(\theta) \triangleq J_{k=1}(\bar{\pi}_{\theta, \phi_{\mathrm{CL}}}) - J_{k=H}(\bar{\pi}_{\theta, \phi_{\mathrm{OL}}})$$
</div>

<!--research-section-splitter-->

