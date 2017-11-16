---
title: "Semi-Supervised Training Using Adversarial Multi-Task Learning for Spoken Language Understanding"
read_time: false
tags:
  - Spoken Language Understanding
  - Multi-Task Learning
  - Semi-Supervised Learning
  - Adversarial Task Discriminator
---

* Submitted to *IEEE International Conference on Acoustics, Speech, and Signal Processing*, 2018, under review.

* Designed a multitask learning method by neatly merging a unidirectional / bidirectional language model and a slot tagging model in SLU.

* Exploited a shared space for both tasks and two task-specific spaces for classification, extracted generalized language knowledge, and regularized the slot tagging model.

* Developed an adversarial discriminator to obtain more task-independent sharing information for SLU.

* Implemented in *PyTorch*.

* Achieved the best performance in slot tagging task on both small (ATIS) and large-scale datasets (e.g. improved F1-score from 67.66% to 71.55% with 5k labeled sentences)
