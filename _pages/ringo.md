---
layout: project
title: "RINGO: Real-time Navigation with a Guiding Trajectory for Aerial Manipulators in Unknown Environments"
permalink: /ringo/
author_profile: false
project_name: RINGO
affiliation: Nankai University
description: Real-time navigation with a guiding trajectory for aerial manipulators in unknown environments.
hide_project_footer: true
project_authors:
  - id: zhaopeng_zhang
  - id: shizhen_wu
  - id: chenfeng_guo
  - id: yongchun_fang
  - id: jianda_han
  - id: xiao_liang
---

<section class="project-section project-abstract" markdown="1">
<h2 id="abstract">Abstract</h2>

Motion planning for aerial manipulators in constrained environments has typically been limited to known environments or simplified to that of multi-rotors, which leads to poor adaptability and overly conservative trajectories. This paper presents RINGO: Real-time Navigation with a Guiding Trajectory, a novel planning framework that enables aerial manipulators to navigate unknown environments in real time. The proposed method simultaneously considers the positions of both the multi-rotor and the end-effector. A pre-obtained multi-rotor trajectory serves as a guiding reference, allowing the end-effector to generate a smooth, collision-free, and workspace-compatible trajectory. Leveraging the convex hull property of B-spline curves, we theoretically guarantee that the trajectory remains within the reachable workspace. To the best of our knowledge, this is the first work that enables real-time navigation of aerial manipulators in unknown environments. The simulation and experimental results show the effectiveness of the proposed method. The proposed method generates less conservative trajectories than approaches that consider only the multi-rotor.

</section>
