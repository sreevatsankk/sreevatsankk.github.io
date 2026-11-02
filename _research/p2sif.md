---
title: "P2SIF: Plug-n-Play Sensor Integration Framework"
seo_title: "P2SIF: LLM Sensor Integration | Sreevatsank Kadaveru"
description: "P2SIF integrates new sensor modalities such as LiDAR and radar into existing LLMs without modifying their weights, using specialist models and text reports."
group: physical-ai
order: 3
image: /images/research/p2sif.webp
image_size: [1100, 671]
image_alt: "P2SIF architecture: specialist models for radar, camera, LiDAR, and GPS feed a knowledge-fusion stage and a generalist LLM"
team: "with Pushkal Mishra and Dinesh Bharadia"
links:
  - label: Proposal
    url: /files/P2SIF_Proposal.pdf
---
General-purpose LLMs reason effectively but cannot interpret raw LiDAR or radar data; in our tests, frontier models reported vehicles in scenes that contained none. Fine-tuning and adapter layers address this only by tying each sensor to one model's weights. P2SIF is a decoupled architecture that integrates new modalities into existing LLMs without modifying their weights. Specialist models convert each sensor stream (camera, LiDAR, radar, GPS) into concise text reports, a knowledge-fusion stage merges them, and an unmodified generalist LLM makes the decision. New sensors can be added without retraining, the LLM can be replaced independently, and each decision leaves a human-readable trail for failure attribution. The target applications are autonomous-driving tasks in CARLA and on real LiDAR, radar, and camera data, including fog and night driving.
