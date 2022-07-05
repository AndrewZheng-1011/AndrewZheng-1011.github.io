---
title: "Physics Informed Neural Network for Quadruped Dynamics "
excerpt: "Leveraging linear operator theory for dynamical systems and neural network as universal function approximator, this neural network architecture aims to identify quadruped dynamics<br/><img src='/images/portfolio/KoopmanAEModel.PNG'>"
collection: portfolio
---

<h2>Introduction</h2>
Neural networks are considered as a universal function approximator as they are capable to approximating any type of function. However, although they are capable, it does not necessarily guarantee that the network learns the right approximation. Therefore, recent research has tried to incorporate physics informed neural networks as a way to guide neural networks to learn a manifold that resembles nonlinear dynamical systems. Some categories to these physics informed neural networks are Lagrangian neural networks, Hamiltonian Neural Networks, and Nueral ODEs. All these applications try to incorporate some "physic-informed" information/structure to learn the manifold associated with their corresponding concepts.
<br>
<br>
Another area of research that has seen recent popularity in modeling dynamical system is Koopman Operator theory. One of its strengths lies in using data driven methods such as Extended Dynamic Mode Decomposition (EDMD) to find a lifting that represents the nonlinear system as a linear dynamical system in the lifted space. One of the difficulties in this method is finding a correct lifting.
<br>
<br>
Additionally, another factor that needs to be considered is the hybrid and nonlinear nature in quadruped leg dynamics. Quadruped leg dynamics is inherently hybrid as it consists of a swing and stance phase, causing discontinuity in the velocity and acceleration and the nonlinear nature stems from the angular orientation of the leg. To address both of these solutions, we use a mix between linear operator theory (Koopman) and neural networks (i.e. neural network's impressive function approximation) to showcase a self-supervised learning of the Koopman operator on quadruped dynamics.

![KoopmanAEModel](/images/portfolio/KoopmanAEModel.PNG)
