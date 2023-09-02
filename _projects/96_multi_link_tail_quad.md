---
title: "Multi-Link Tail Controller on Legged Locomotion"
excerpt: <img src='/images/projects/multi_link_tail/two_tail_switch_control.gif'/>
collection: projects
---
# Summary
<p align="center">
  <img src='/images/projects/multi_link_tail/tail_control_diagram.png'/>
</p>


Quadrupeds have seen great success in traversing through rough terrains. However, despite its success in locomotion, there still exists challenges for quadrupeds in contact-critical environments.
In other words, there are challenges for legged robots in environments where one slight misstep, could cause fatal damage to the robot. Due to the underactuated nature of quadrupeds, a natural suggestion is to append a tail as an extra
actuator to increase the freedom of movement. Inspired by cat-like motions, this project incorporates a 2 degree of freedom (DoF) tail, in which the work uses a time-based switching controller
to achieve better landing rates in contact critical terrains. A diagram of the control scheme is seen. For more details, see the following [paper](https://github.com/AndrewZheng-1011/AndrewZheng-1011.github.io/blob/master/docs/Analysis_of_Open_Loop_Tail_Control_On_Quadruped_Locomotion_in_Contact_Critical_Terrains.pdf).
## Results
<p align="center">
  <img src='/images/projects/multi_link_tail/two_tail_switch_control.gif'/>
</p>


We show results of the legged robot walking nominally off the terrain. As seen, the controller actuates during freefall, orienting the rigid body towards a stable position. As it approaches
the ground, it lands on four legs, continuing its trot. To run the following code, see the following [repository](https://github.com/AndrewZheng-1011/quad-sdk/tree/add-multi-link-tail-controller).
