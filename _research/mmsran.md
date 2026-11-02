---
title: "mmsRAN: Multimodal Cellular Uplink for Physical AI"
seo_title: "mmsRAN: Multimodal Cellular Uplink | Sreevatsank Kadaveru"
description: "mmsRAN is a 5G uplink scheduler that delivers multimodal sensor flows for Physical AI with low latency and in lock-step. Work in progress at ACM MobiCom 2026."
group: physical-ai
order: 4
period: "2025 – present"
image: /images/research/mmsran.webp
image_size: [1500, 595]
image_alt: "mmsRAN scheduling loop: the edge application shares future sensing decisions and an EdgeRIC app schedules each user's sensor streams per RAN slot"
figure: wide
badges: ["Qualcomm Innovation Fellowship 2026", "WiP · ACM MobiCom 2026"]
team: "with Ushasi Ghosh, Srinivas Shakkottai, and Dinesh Bharadia"
links:
  - label: Paper
    url: https://doi.org/10.1145/3795866.3844782
  - label: EdgeRIC Page
    url: https://edgeric.ucsd.edu/projects/multimodal-sensing.html
---
A robot's control loop operates in discrete timesteps, and the edge application can act only once every sensor stream for a timestep has arrived. Over the cellular uplink, these streams arrive skewed, both across one robot's sensors and across robots sharing a cell; in our multi-user measurements, skew alone adds approximately 13 ms of latency. mmsRAN is an uplink scheduler for multimodal sensor flows that must be low latency, synchronized, and delivered in lock-step. Each sensor modality receives its own QoS flow and data radio bearer, and a scheduler running on EdgeRIC allocates uplink resources per slot so that a timestep's streams arrive together. In early over-the-air results on our 5G testbed, network tuning reduced median sensor-frame latency from 30.4 ms to 18.9 ms, and bearer-level prioritization roughly halved the latency of a high-priority stream without starving the others.
