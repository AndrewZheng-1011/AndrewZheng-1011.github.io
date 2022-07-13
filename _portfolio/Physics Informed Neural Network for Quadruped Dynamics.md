---
title: "Physics Informed Neural Network for Quadruped Dynamics "
excerpt: "Leveraging linear operator theory for dynamical systems and neural network as universal function approximator, this neural network architecture aims to identify quadruped dynamics<br/><img src='/images/portfolio/KoopmanAEModel.PNG'>"
collection: portfolio
---

<h2>Introduction</h2>
Quadruped leg dynamics are hybrid, nonlinear,  and high dimensional, causing many current approaches to modeling quadruped dynamics through linearization or reduced ordered models. This causes many traditional locomotion of legged robots consist of using hierarchal control to generate a feasible center of mass trajectory with a global planner used on a reduced model and a lower level control to deal with higher fidelity model.
In this work, we (DIRA research lab) attempt to use Koopman operator theory as means to deal with the nonlinear hybrid leg dynamics of quadruped and neural networks as a a method to find the high dimensional lifting of the linear operator. This work focuses on system analysis of quadruped leg dynamics using the Koopman operator and showcasing the limits of the linear operator theory. 

<h2> Brief Overview </h2>
![KoopmanLifting](/images/portfolio/KoopmanLifting.PNG)
The Koopman operator theory consists of finding a lifting (i.e. mapping to a infinite, or high in practice, dimensional space) where the dynamics of the system is represented linearly. Thus, the rich history in linear system analysis and our tools to analyze linear systems can be used. However, finding this lifting is not trivial. Thus, by combining the neural network framework, a great function approximation tool, we can negate the daunting task of finding the right lifted space. Note, the demerit to this methodology is that the lifting is a black box and there is not a explicit expression for this lifted space.

<h2> Methodology </h2>
The quadruped locomotion was simulated in gazebo simulation using the champ quadruped model. A automated simulation testbed was generated (can run simulation testbed <a href = "https://github.com/AndrewZheng-1011/terrain_champ" title="terrain_champ">here</a>) to conduct quadruped locomotion under the following parameters shown in the table below:
![gazeboTableSimParams](/images/portfolio/gazeboChampSimParams.PNG)

![KoopmanAEModel](/images/portfolio/KoopmanAEModel.PNG)
<h2> Results & Conclusion </h2>
