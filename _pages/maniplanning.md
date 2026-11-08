---
layout: project
title: "A Collision-Aware Motion Planning Framework With Goal State Generation for Aerial Manipulation in Constrained Environments"
permalink: /maniplanning/
author_profile: false
project_name: ManiPlanning
affiliation: Nankai University
description: Collision-aware whole-body motion planning for aerial manipulation in constrained environments.
venue: IEEE Transactions on Industrial Electronics, early access, 2026
project_authors:
  - id: zhaopeng_zhang
  - id: hai_yu
  - id: wei_he
  - id: yongchun_fang
  - id: jianda_han
  - id: xiao_liang
resources:
  - label: Paper
    url: https://doi.org/10.1109/TIE.2026.3748210
  - label: PDF
    url: /files/TIE-2026.pdf
  - label: Code
    url: https://github.com/cheungsiupaang/ManiPlanner
  - label: Video
    url: https://www.youtube.com/watch?v=sBdlaGuF9AE
video_id: sBdlaGuF9AE
demo_caption: Whole-body aerial manipulation in constrained environments.
---

<section class="project-section project-abstract" markdown="1">

## Abstract
{: #abstract }

In this article, we propose a collision-aware motion planning framework with goal state generation (GSG) for aerial manipulation in constrained environments. The framework generates nominal trajectories that satisfy the collision checks and are dynamically consistent. Owing to the kinematic redundancy of aerial manipulators, a given end-effector (EE) pose can correspond to multiple feasible system states. We introduce a collision-avoidance margin concept that quantifies the collision risk for aerial manipulators, and generate an optimal goal state by minimizing it while satisfying the target EE pose and collision-avoidance constraints. Then, a goal-state-biased path searching algorithm is developed in configuration space, where the generated optimal goal state guides the search to efficiently obtain a whole-body path that passes the geometric collision checks, and a weighted-sum cost is adopted to properly measure the distance between states. Finally, the generated path is converted into a dynamically consistent trajectory satisfying feasibility constraints for the flat outputs of the aerial manipulator by solving a gradient-based optimization problem that incorporates both collision-avoidance constraints and feasibility constraints, including velocity limits, acceleration limits, joint-angle limits, and maximum tilt-angle limit. The proposed method incorporates a geometrically accurate whole-body collision model for aerial manipulation, which explicitly accounts for the full geometry of both the multirotor and the robotic arm through multiple sets of spheres, supporting whole-body collision avoidance in constrained environments. The proposed motion planning framework is validated and shown to be effective in both simulation and real-world experiments.

</section>

<section class="project-section" markdown="1">

## Contributions
{: #contributions }

The framework addresses whole-body motion planning for aerial manipulators operating with limited obstacle clearance. Its main contributions are:

- **Collision-aware goal state generation.** The planner exploits kinematic redundancy to select a favorable goal state by minimizing the whole-body collision margin while satisfying the desired end-effector pose. This goal state guides the subsequent path search and trajectory optimization.
- **Link-level whole-body collision modeling.** Multiple sets of spheres represent the multirotor and individual arm links. An adjustment for the underactuated platform provides a theoretically guaranteed collision margin under bounded tilt motion.
- **Dynamically consistent trajectory optimization.** The optimizer uses the flat outputs of the complete aerial-manipulator system, with its center of mass as the position component, and incorporates whole-body collision avoidance and motion feasibility constraints.

</section>

<section class="project-section" markdown="1">

## Framework
{: #framework }

Given the initial state, target end-effector pose, and an ESDF map, the planner proceeds through three stages: goal state generation, configuration-space path searching, and spatial-temporal trajectory optimization. The searched path initializes the optimization of the complete system's flat-output trajectory.

<figure class="project-figure project-figure--framework">
  <a href="{{ '/assets/images/projects/maniplanning/framework.png' | relative_url }}">
    <img src="{{ '/assets/images/projects/maniplanning/framework.png' | relative_url }}" width="1408" height="616" loading="lazy" alt="ManiPlanning framework: target pose, start state and ESDF map feed goal state generation, path searching and collision-aware trajectory optimization.">
  </a>
  <figcaption>Method overview (Fig. 3 in the paper). Goal state generation and path searching operate in configuration space; trajectory optimization operates on the spatial-temporal parameters of the flat outputs.</figcaption>
</figure>

</section>

<section class="project-section" markdown="1">

## Results
{: #results }

<div class="project-results-grid">
  <figure class="project-figure">
    <video width="1920" height="1080" autoplay controls muted loop playsinline preload="metadata" aria-label="ManiPlanning experiment demonstration 1">
      <source src="{{ '/publications/maniplanning/maniplanning-1.mp4' | relative_url }}" type="video/mp4">
      <a href="{{ '/publications/maniplanning/maniplanning-1.mp4' | relative_url }}">Watch ManiPlanning demonstration 1.</a>
    </video>
  </figure>
  <figure class="project-figure">
    <video width="1920" height="1080" autoplay controls muted loop playsinline preload="metadata" aria-label="ManiPlanning experiment demonstration 2">
      <source src="{{ '/publications/maniplanning/maniplanning-2.mp4' | relative_url }}" type="video/mp4">
      <a href="{{ '/publications/maniplanning/maniplanning-2.mp4' | relative_url }}">Watch ManiPlanning demonstration 2.</a>
    </video>
  </figure>
</div>

</section>
