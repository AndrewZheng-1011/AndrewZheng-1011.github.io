---
title: "Perceptive Locomotion on Unstructured Terrain"
excerpt: <img src='/videos/perceptive_locomotion_unstructured_terrain/experimental_stairs_static_walk_view.gif' />
collection: portfolio
---
# Summary
<p align="center">
    <img src="/images/portfolio/perceptive_locomotion_unstructured_terrain/legged_locomotion_adaptation_module.png" />
</p>
As shown in the schematic diagram above, this work utilizes a Legged Locomotion Adaptation Module to modify reference trajectories for legged locomotion given map information. 
By utilizing map information that describes the geometry, edge, and traversability of the environment and a high level motion command, this work categorizes the locomotion problem into two motion trajectories that are to be transformed:
1. The center of mass trajectory for generic motion planning of a single rigid body over rough terrains
2. Foothold / Swing Trajectory of the leg over rough terrains

These trajectories are then used in the model predictive controller to find locally optimal solutions under dynamic system constraints. The following optimal control solution is then executed onto the robot, giving the next state, and thus, reiterates the method in real-time.

As a result, the methodology of adapting the trajectory to be locally optimized in the nonlinear model predictive controller (NMPC) works adequately well for the quadruped to walk over terrains such as ramps, stairs, pits, etc. Results can be seen in the subsection below, along with a case of failure.
## Simulation Results
Simulation results of quadruped in a environment with stairs of 10cm in height and 20cm in depth.
<video width="720" height="480" controls="controls">
    <source src="/videos/perceptive_locomotion_unstructured_terrain/stairs_10cm_default_ee_pos_cost.mp4" type="video/mp4">
</video>

## Hardware Results
Hardware results w/ static walking gait for stairs of 6-12cm in height and 25cm in depth.
<video width="720" height="400" controls="controls">
    <source src="/videos/perceptive_locomotion_unstructured_terrain/experimental_stairs_static_walk_view.mp4" type="video/mp4">
</video>

## Failure Cases
Hardware results w/ trot gait for stairs of 6-12cm in height and 25cm in depth.
<video width="720" height="480" controls="controls">
    <source src="/videos/perceptive_locomotion_unstructured_terrain/experimental_stairs_trot.mp4" type="video/mp4">
</video>

# Methodology


# Discussions

# Conclusions
