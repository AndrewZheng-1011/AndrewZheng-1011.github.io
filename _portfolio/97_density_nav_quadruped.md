---
title: "Density Navigation for Quadruped Locomotion"
excerpt: <img src='/images/portfolio/density_nav_quadruped/go1_hw_fb_density_planner.gif' width='640' height='360'/>
collection: portfolio
---

# Summary
<p align="center">
  <img src='/images/portfolio/density_nav_quadruped/quad_diagram.png'/>
</p>
This project incorporates the density formulation from the following paper submitted to Robotics Automations and Letters (RA-L), titled "Safe Navigation Using Density Function: Analytical Construction" onto quadrupeds.
It incorporates the high level plan of the following dynamics $\dot x = u$ and maps to a centroidal reference trajectory of the following dynamic form:


$$\mathbf{M}(\ddot{\mathbf{q}}) + \mathbf{C}(\mathbf{q}, \dot{\mathbf{q}}) + \mathbf{G}(\mathbf{q}) = \mathbf{B}(\mathbf{q})\mathbf{\tau}$$

where $\mathbf{M}$ is the inertial matrix, $\mathbf{C}$ contains the centripetal and coriolis terms, $\mathbf{G}$ is the gravitational field, $\mathbf{B}$ is the control matrix, $\mathbf{\tau}$ is the joint torques, and $\mathbf{q} \in \mathbb{R}^{24}$ are the states for the dynamical system. This is then incorporated into a nonlinear model predictive controller (NMPC), where the optimized control trajectory is tracked with a torque-level control. The schematic diagram describes the process.

The main contribution of this work integrates the novel formulation of density for safe navigation using the modular [legged planner](https://github.com/AndrewZheng-1011/legged_planner) framework. As a result, we are able to incorporate safe navigation using density for quadrupeds. For more detailed information, see the following [paper](https://github.com/AndrewZheng-1011/AndrewZheng-1011.github.io/blob/master/docs/Motion_Planning_for_Quadruped_Robots_using_Density_Functions.pdf).

## Results
We show results in both simulations and hardware. In simulation, we show the quadruped navigating around multiple obstacles.
<video width="720" height="480" controls="controls">
    <source src="/images/portfolio/density_nav_quadruped/go1_density_nav_2obs_2x.mp4" type="video/mp4">
</video>

\
We then show on hardware, where the density motion plan navigates around the chair (obstacle) and goes towards the goal, which is tracked using a NMPC.

<video width="720" height="480" controls="controls">
    <source src="/images/portfolio/density_nav_quadruped/go1_hw_feedback_density_planner.mp4" type="video/mp4">
</video>
