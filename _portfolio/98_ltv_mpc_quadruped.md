---
title: "Linear Time-Varying MPC for Quadruped Locomotion"
excerpt: <img src='/images/portfolio/ltv_mpc_quadruped/edited_states_turn_trot.gif' width='660' height='390'/>
collection: portfolio
---

## Summary
This project formulates the heavily used MIT cheetah convex model predictive controller (MPC) for quadruped locomotion. We linearize across the reference trajectory and use a single-shooting method to formulate the optimal control problem under dynamic constraints as a convex model predictive controller. For more details, see our [arxiv paper](https://arxiv.org/pdf/2212.05154.pdf).

## Results
Our results can be seen in our [github repository](https://github.com/AndrewZheng-1011/Quad_ConvexMPC/tree/main). We showcase here the quadruped tracking a reference trajectory to move diagonally across the plane. The corresponding MPC optimizes the reference trajectory, giving corresponding ground reaction force (GRFs) as the control input.
<p align="center">
  <img src='/images/portfolio/ltv_mpc_quadruped/edited_states_turn_trot.gif' width='660' height='390'/>
</p>