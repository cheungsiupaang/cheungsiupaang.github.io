---
layout: single
title: "A Collision-Aware Motion Planning Framework With Goal State Generation for Aerial Manipulation in Constrained Environments"
permalink: /maniplanning/
author_profile: true
---

**Zhaopeng Zhang**, [Hai Yu](https://u-hai.github.io/), Wei He, Yongchun Fang, Jianda Han*, and Xiao Liang*

*IEEE Transactions on Industrial Electronics*, early access, 2026

---

This work proposes a collision-aware whole-body motion planning framework for aerial manipulation in constrained environments. Given a target end-effector pose, the framework selects a favorable goal state, searches for a whole-body path, and optimizes a dynamically consistent trajectory. A link-level collision model accounts for the geometry of both the multi-rotor and the robotic arm, enabling manipulation in confined spaces. The framework is validated in both simulation and real-world experiments.

## Key Features

- **Collision-Aware Goal State Generation**: Exploits kinematic redundancy to select a goal state that minimizes a collision-avoidance margin while satisfying the target end-effector position and orientation
- **Whole-Body Path Searching**: Uses a goal-state-biased bidirectional RRT* search with a weighted configuration-space distance to connect the initial state to the generated goal state
- **Link-Level Collision Modeling**: Represents the multi-rotor and individual arm links with multiple sets of spheres, with an adjustment to account for platform tilt during motion
- **Dynamically Consistent Trajectory Optimization**: Uses the complete system's flat outputs, including its center of mass, to account for dynamic coupling while incorporating collision avoidance and motion feasibility constraints

<iframe width="400" height="225"
        src="https://www.youtube.com/embed/sBdlaGuF9AE"
        title="YouTube video player"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
        allowfullscreen>
</iframe>

## Links

- [IEEE Paper](https://doi.org/10.1109/TIE.2026.3748210)
- [PDF Download](/files/TIE-2026.pdf)
- [Code Repository](https://github.com/cheungsiupaang/ManiPlanner)
