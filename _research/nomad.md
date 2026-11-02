---
title: "Nomad: Providing Insights into the Spectrum Environment"
seo_title: "Nomad: 40 Gbit/s Spectrum Sensing | Sreevatsank Kadaveru"
description: "Nomad is a high-throughput spectrum sensing system with a 40 Gbit/s line rate, built from containerized microservices. Published at ACM MobiCom 2024."
group: spectrum
order: 4
period: "2022 – 2024"
teaser: "A high-throughput spectrum sensing system with a line rate of 40 Gbit/s. I architected its pipeline, built from containerized microservices for buffering, signal detection, and classification."
image: /images/research/nomad.webp
image_size: [1100, 551]
image_alt: "Nomad architecture: an API controller and FIFO buffer feed I/Q samples through shared memory to signal-detection and classifier containers that share a GPU, coordinated by a command-and-control database and an RF scheduler"
badges: ["IARPA-funded", "ACM MobiCom 2024"]
links:
  - label: Paper
    url: https://doi.org/10.1145/3636534.3698867
  - label: Signals Lab Page
    url: https://wcsng.ucsd.edu/signals-lab/project/nomad/
---
The microservices exchange samples through a copy-efficient shared-memory interface and coordinate through a Redis-based in-memory database.
