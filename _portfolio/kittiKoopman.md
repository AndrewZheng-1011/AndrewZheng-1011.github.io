---
title: "Trajectory Prediction using Real-Time Koopman Operator"
excerpt: "Usage of KITTI's multi-object tracking dataset using an online variant of Koopman Operator<br/><img src='/images/portfolio/ODMD_KITTI_Pipeline.PNG' alt='Pipeline for ODMD with Koopman on KITTI Dataset'>"
collection: portfolio
---

<h2> Introduction </h2>
Prediction of environmental dynamics (i.e. static and dynamic obstacles) and corresponding tracking of these obstacles have seen many applications in the computer vision side. Moreso, with the rise in machine learning and deep learning algorithms, many of the current frameworks uses these frameworks as a means to predict obstacle dynamics in structured or unstructured environments. However, all these methods generally remain a black box and not much analysis can be done to understand the ongoing dynamics of the obstacles. In constrast, the Koopman operator is a great tool for analyzing nonlinear system behavior through data driven means. In this paper, we use a real time Koopman operator to learn system dynamics of detected obstacles on the KITTI dataset and use spectral theory to glimpse at the dominant eigen modes of detected obstacles. 

<h2> Koopman Operator </h2>
The Koopman operator is an infinite dimensional operator that propagates its observables linearly in the lifted space. This is expressed in the form
<br/><br/>
$[\mathcal{K}g] (x) := g\circ F(x) = g(x_{k+1})$
<br/><br/>
Most data driven methods will then solve the Koopman operator using DMD or EDMD which involves taking the pseudo inverse of the observables to compute the Koopman operator ($\mathcal{K}$):
<br/><br/>
$\mathcal{K} = \Psi(Y)\Psi(X)^{\dagger}$
<br/><br/>
where $X$ and $Y$ $\in \mathbb{R}^{n\times m}$ where n and m is the dimension of the states and the number of discrete datapoints (i.e. snapshots). Correspondingly, the observables $\Psi(X)$ and $\Psi(Y) \in \mathbb{R}^{N\times m}$ are the observables where N is the lifted dimension. However, this formulation only involves an offline case where every new set of snapshots (x,y) involves recomputing the Koopman operator, involving a computationally expensive pseudo inverse. Therefore, an online variant of the Koopman operator takes a stream of datapoints and updates the operator through a means similar to recursive least squares (i.e. [Online Dynamic Mode Decomposition](https://arxiv.org/pdf/1707.02876.pdf))
![odmdKittiPipeline](/images/portfolio/ODMD_KITTI_Pipeline.PNG)
<br/>
The following formulation of Online Dynamic Mode Decomposition (ODMD) comes to the following form:
<br/><br/>
$A_k = (Y_kX_k)(X_kX_k^T)^{-1} = Q_kP_k$
$A_{k+1} = A_k + \gamma_{k+1}(y_{k+1}-A_kx_{k+1})x_{k+1}^T P_k$
<br/><br/>
where $A_k$ is the computed Koopman operator, k is the number of snapshots, and $\gamma_{k+1}$ is
<br/><br/>
$\gamma_{k+1} = \frac{1}{1+x_{k+1}^TP_kx_{k+1}}$
<br/><br/>
Additionally, to recursively update $A_k$, the following matrix $P_k$ needs to be updated with the following form:
<br/><br/>
$P_{k+1} = P_k-\gamma_{k+1}P_kx_{k+1}x_{k+1}^T P_k$
<br/><br/>

Notice, that after computing the Koopman operator, there is no additional computation of the inverse calculation for the operator. Other variations of the ODMD algorithm forgets older snapshots to aid in incorporating time varying dynamics. These algorithms were then tested on a stream of data from the KITTI dataset.

<h2> Results </h2>
![Time0KITTIKoopman](/images/portfolio/0000 (3).jpg)
![Time7KITTIKoopman](/images/portfolio/0007.jpg)
![Time50KITTIKoopman](/images/portfolio/0050.jpg)
![Time75KITTIKoopman](/images/portfolio/0075.jpg)
