---
title: "rfYOLO: Phase as a Modality for Signal Detection"
seo_title: "rfYOLO: Phase for Signal Detection | Sreevatsank Kadaveru"
description: "rfYOLO studies phase as an additional modality for PHY-layer signal detection, using a transform that improves signal characterisation with YOLO networks."
group: spectrum
order: 3
period: "2022 – 2024"
teaser: "A phase transform that improves PHY-layer signal characterisation using YOLO networks. rfYOLO studies phase as an additional modality, since spectrogram-based detectors discard phase information."
image: /images/research/rfyolo.webp
image_size: [1500, 918]
image_alt: "Top: the same signal shown as an STFT magnitude, raw STFT phase, and normalized phase. Bottom: the yoLight pipeline, in which a fast energy detector gates YOLO and Searchlight boxes the remainder."
badges: ["IARPA-funded"]
---
On a mixed dataset, YOLO on STFT magnitude alone identified CPFSK, FSK, and GFSK at 90–96% and PSK2 at 83%, likely because their spectral shapes differ, but could not separate QAM orders (26–32%). The transform removes the deterministic phase term introduced by the STFT and weights the result by magnitude. Raw STFT phase proved ineffective as a network input, while the corrected phase performed better. The surrounding pipeline, yoLight, uses a fast energy detector to gate YOLO inference, subtracts YOLO's detections from the stream, and passes the remainder to the Searchlight energy detector to produce boxed IQ and signal metadata.
