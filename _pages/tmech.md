---
layout: project
title: "An End-Effector-Oriented Coupled Motion Planning Method for Aerial Manipulators in Constrained Environments"
permalink: /tmech/
author_profile: false
project_name: End-Effector-Oriented Coupled Motion Planning
affiliation: Nankai University
description: Coupled motion planning for aerial manipulators with end-effector position and orientation constraints.
venue: IEEE/ASME Transactions on Mechatronics, 30(6):6027–6037, 2025
project_authors:
  - id: zhaopeng_zhang
  - id: hai_yu
  - id: yi_chai
  - id: zhichao_yang
  - id: xiao_liang
  - id: yongchun_fang
  - id: jianda_han
resources:
  - label: Paper
    url: https://ieeexplore.ieee.org/document/10943237
  - label: PDF
    url: /files/TMech.pdf
  - label: Code
    url: https://github.com/cheungsiupaang/Safe-Planner
  - label: Video
    url: https://www.youtube.com/watch?v=0KmbkZefSSk
video_id: 0KmbkZefSSk
demo_caption: End-effector-oriented coupled motion planning in constrained environments.
---

<section class="project-section project-abstract" markdown="1">

## Abstract

The aerial manipulator, composed of a multirotor and a robotic arm, could provide extra active operation capability and has the potential for applications in both military and civilian fields. Due to the complex working scenarios, planning a safe and reliable motion trajectory for aerial manipulators is of great importance. To achieve target grasping with aerial manipulators in complex environments, a coupled motion planning method for the aerial manipulator is proposed in this article, which conducts the motion planning for the multirotor and the robotic arm simultaneously. Specifically, the aerial manipulator is considered as enclosed by a convex polyhedron other than a big sphere so as to reduce the conservatism of the trajectory. Furthermore, the trajectory of the aerial manipulator could be represented by a set of polynomial functions of the flat outputs, including the position and the yaw angle of the multirotor and the joint angles of the robotic arm. Utilizing polynomial-based trajectory representation for both the multirotor's and the robotic arm's states simplifies the optimization problem and ensures dynamic feasibility. The simulation and experimental results show the effectiveness of the proposed method. Unlike the other works that only consider the position of the end-effector, the proposed method also takes into account the orientation of the end-effector as well, resulting in improved performance in grasping tasks.

</section>

<section class="project-section" markdown="1">

## Contributions

The method jointly plans the multirotor and robotic arm trajectories for end-effector-oriented manipulation. Its main contributions are:

- **A dynamic convex polyhedron for collision avoidance.** The aerial manipulator is enclosed by a polyhedron that changes with its configuration, reducing the conservatism of a large spherical envelope. A spherical envelope can make motion planning fail in some constrained environments.
- **End-effector position and orientation constraints.** The desired orientation is considered together with the desired position, helping the end-effector avoid collisions with the target object during grasping.

</section>

<section class="project-section" markdown="1">

## Framework

The planner represents the multirotor position, yaw angle, and robotic arm joint angles with polynomial trajectories. It combines initial and goal state constraints, trajectory continuity, dynamic limits, and a collision constraint that keeps the dynamic convex polyhedron within a safe flight corridor. These constraints enter one optimization problem to generate the multirotor and arm trajectories simultaneously.

<figure class="project-figure project-figure--framework">
  <a href="{{ '/assets/images/projects/tmech/framework.png' | relative_url }}">
    <img src="{{ '/assets/images/projects/tmech/framework.png' | relative_url }}" width="1000" height="564" loading="lazy" alt="Trajectory optimization framework combining initial and goal states, continuity, dynamic convex polyhedron safety constraints, and dynamic limits to generate multirotor and arm trajectories simultaneously.">
  </a>
  <figcaption>Trajectory optimization framework. <a href="{{ '/files/TMech.pdf' | relative_url }}#page=4">Figure 3 in the paper.</a></figcaption>
</figure>

</section>

<section class="project-section" markdown="1">

## Results

<div class="project-results-grid">
  <figure class="project-figure">
    <video width="1920" height="1080" autoplay controls muted loop playsinline preload="metadata" aria-label="SafePlanning experiment demonstration 2-1">
      <source src="{{ '/publications/safeplanning/safeplan-2-1.mp4' | relative_url }}" type="video/mp4">
      <a href="{{ '/publications/safeplanning/safeplan-2-1.mp4' | relative_url }}">Watch SafePlanning demonstration 2-1.</a>
    </video>
  </figure>
  <figure class="project-figure">
    <video width="1920" height="1080" autoplay controls muted loop playsinline preload="metadata" aria-label="SafePlanning experiment demonstration 2-2">
      <source src="{{ '/publications/safeplanning/safeplan-2-2.mp4' | relative_url }}" type="video/mp4">
      <a href="{{ '/publications/safeplanning/safeplan-2-2.mp4' | relative_url }}">Watch SafePlanning demonstration 2-2.</a>
    </video>
  </figure>
</div>

</section>
