---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}

<!--## Publications -->
0. **Safe Navigation Using Analytical Density Functions** \
   Andrew Zheng, Sriram S.K.S. Naryanan, and Umesh Vaidya. _IEEE Robotics and Automation Letters (RA-L) (2023)_. [Link](https://ieeexplore.ieee.org/abstract/document/10238751)
0. **Off-Road Navigation of Legged Robots Using Linear Transfer Operators**\
   Joseph Moyalan, Andrew Zheng, Sriram S.K.S. Narayanan, and Umesh Vaidya. Accepted at _Model, Estimation, and Control Conference (MECC)_. **ASME DSCD Robotics Best Paper Award**. [Link](https://arxiv.org/pdf/2305.02938.pdf)
0. **Artificial Neural Network Based Terrain Reconstruction for Off-road Autonomous Vehicles Using LiDAR** \
   Sarang Sutavani, Andrew Zheng, et al. Submitted to _Ground Vehicle Systems Engineering and Technology Symposium (GVSET)_.
0. **Modeling Quadruped Leg Dynamics on Deformable Terrain using Data-Driven Koopman Operators**\
   Alexander Krolicki, Dakota Rufino, Andrew Zheng, Sriram S.K.S. Narayanan, Jackson Erb, and Umesh Vaidya. Submitted to _IFAC-PapersOnLine 55.37 (2022): 420-425_. [Link](https://www.sciencedirect.com/science/article/pii/S2405896322028622)

