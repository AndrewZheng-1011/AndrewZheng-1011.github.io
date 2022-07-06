---
title: "Trajectory Prediction using Real-Time Koopman Operator"
excerpt: "Usage of KITTI's multi-object tracking dataset using an online variant of Koopman Operator<br/><img src='/images/portfolio/Object Detection Pic.png'>"
collection: portfolio
---

<h2> Introduction </h2>
Prediction of environmental dynamics (i.e. static and dynamic obstacles) and corresponding tracking of these obstacles have seen many applications in the computer vision side. Moreso, with the rise in machine learning and deep learning algorithms, many of the current frameworks uses these frameworks as a means to predict obstacle dynamics in structured or unstructured environments. However, all these methods generally remain a black box and not much analysis can be done to understand the ongoing dynamics of the obstacles. In constrast, the Koopman operator is a great tool for analyzing nonlinear system behavior through data driven means. In this paper, we use a real time Koopman operator to learn system dynamics of detected obstacles on the KITTI dataset and use spectral theory to glimpse at the dominant eigen modes of detected obstacles. 

<h2> Preliminaries </h2>
<h3> Real time Koopman Operator </h3>
[!odmdKittiPipeline](/images/portfolio/ODMD_KITTI_Pipeline.PNG)


Note: Put citations
