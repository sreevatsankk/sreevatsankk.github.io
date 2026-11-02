---
title: "PHYNet: A Gold-Standard Labelled PHY-Layer Dataset"
seo_title: "PHYNet: Labelled PHY-Layer Dataset | Sreevatsank Kadaveru"
description: "PHYNet is a multi-purpose labelled PHY-layer dataset of over-the-air captures across Wi-Fi, BLE, Zigbee, LoRa, and 5G, for evaluating PHY-layer algorithms."
group: spectrum
order: 1
period: "2024 – 2026"
teaser: "A multi-purpose labelled PHY-layer dataset that establishes a standard for evaluating PHY-layer algorithms. PHYNet labels transmissions in over-the-air captures using hardware sniffers for Wi-Fi, BLE, Zigbee, LoRa, and 5G alongside GNU Radio transmitters."
image: /images/research/phynet.jpg
image_size: [1530, 442]
image_alt: "The same over-the-air capture labelled two ways: PHYNet's ground truth marks each transmission, while an energy detector merges some bursts and fragments others"
---
Real-world PHY datasets are typically limited to RF fingerprinting for a single protocol. Hardware timestamps and clock-drift correction align PHYNet's labels to within approximately 2 µs of the IQ samples, and a successive decoding and cancellation pipeline recovers weaker transmissions. The labels support benchmarking of energy detection, modulation recognition, RF fingerprinting, and source identification, and were used to study how little current spectrum-awareness tools capture of real spectrum activity.
