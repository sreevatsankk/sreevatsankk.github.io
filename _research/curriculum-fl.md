---
title: "When Do Curricula Work in Federated Learning?"
seo_title: "Curricula in Federated Learning | Sreevatsank Kadaveru"
description: "An ICCV 2023 paper showing that curriculum learning can significantly improve convergence in federated learning and offset the effect of non-IID data."
group: earlier
order: 1
period: "2022"
teaser: "A study of curriculum learning in a federated context, showing that curricula can significantly improve the convergence time of training. Ordered learning substantially offsets the effect of non-IID data, and clients with more divergent distributions benefit more."
image: /images/research/curriculum-fl.webp
image_size: [600, 324]
image_alt: "Illustration of training data split across two clients and an easy-first curriculum"
badges: ["ICCV 2023"]
team: "with Saeed Vahidian, Mubarak Shah, Bill Lin, and others"
links:
  - label: Paper
    url: https://openaccess.thecvf.com/content/ICCV2023/html/Vahidian_When_Do_Curricula_Work_in_Federated_Learning_ICCV_2023_paper.html
  - label: arXiv
    url: https://arxiv.org/abs/2212.12712
---
Curriculum learning orders training data from easy to hard, while in federated learning each client trains on its own skewed slice of the data. A convergence analysis models curriculum training as local SGD with locally biased gradients, and a curriculum over clients, introduced from easy to hard, further improves performance.
