---
title: "Perceptive Locomotion on Unstructured Terrain"
excerpt: <img src='/videos/perceptive_locomotion_unstructured_terrain/stairs_10cm_default_ee_pos_cost.gif' />
collection: portfolio
---
# Summary
This work utilizes adaptation of reference trajectories for legged locomotion given map information. 
By utilizing the map information that describes the geometry, traversability, and etc. of the quadruped, we adapt the trajectories of the quadruped. 
As legged locomotion traditionally decouples the problem, the two main trajectories that were modified are:
1. The center of mass trajectory for generic motion planning of quadruped over the rough terrain
2. Foothold / Swing Trajectory of the leg

As a result, the methodology of adapting the reference trajectory works adequately well for the quadruped to walk over terrains such as ramps, stairs, pits, etc. Results can be seen in the video below:

<video width="720" height="480" controls="controls">
    <source src="/videos/perceptive_locomotion_unstructured_terrain/stairs_10cm_default_ee_pos_cost.mp4" type="video/mp4">
</video>
