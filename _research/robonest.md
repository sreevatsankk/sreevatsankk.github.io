---
title: "RoboNEST: Robotics Networked Edge Systems Testbed for Physical AI"
seo_title: "RoboNEST: Physical AI Edge Testbed | Sreevatsank Kadaveru"
description: "RoboNEST is an end-to-end Physical AI testbed that connects real robots, Ethernet, Wi-Fi 6, and private 5G networks, and edge GPUs. Demo at ACM MobiCom 2026."
group: physical-ai
order: 1
period: "2025 – present"
image: /images/research/robonest.webp
image_size: [1600, 414]
image_alt: "RoboNEST testbed: robot arms and a TurtleBot, Ethernet, Wi-Fi and private 5G access networks, and edge GPU compute"
figure: wide
badges: ["Demo · ACM MobiCom 2026"]
team: "with Ushasi Ghosh and Dinesh Bharadia"
links:
  - label: Paper
    url: https://doi.org/10.1145/3795866.3848480
  - label: EdgeRIC Page
    url: https://edgeric.ucsd.edu/projects/robonest.html
---
RoboNEST is an end-to-end testbed that brings real robots, interchangeable access networks, and edge GPUs into one instrumented platform, making the complete sensing-to-action path of a Physical AI task observable and controllable. Two xArm7 arms, SO-101 leader-follower arms, and a TurtleBot stream camera, LiDAR, depth, and IMU data to the edge over Ethernet, Wi-Fi 6, or a private 5G network running [EdgeRIC](https://edgeric.ucsd.edu/). Vision-language-action (VLA) policies run there on GPUs ranging from A10s to an RTX 6000 and a GB10. Clock-synchronized logging correlates application events with RAN state, modem diagnostics, and GPU inference. On a 1080p manipulation task over 5G, moving the policy from an A10 to an RTX 6000 reduces glass-to-action latency from 179 ms to 111 ms; on the same GPU, Wi-Fi and Ethernet reach 77 ms and 68 ms.
