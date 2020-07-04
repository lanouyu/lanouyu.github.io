---
title: "Semi-Supervised Training Using Adversarial Multi-Task Learning for Spoken Language Understanding"
read_time: false
toc: true
tags:
  - Spoken Language Understanding
  - Multi-Task Learning
  - Semi-Supervised Learning
  - Adversarial Task Discriminator
---

Ouyu Lan, Su Zhu, and Kai Yu

*ICASSP, 2018*

[Paper](https://speechlab.sjtu.edu.cn/papers/oyl11-lan-icassp18.pdf){: .btn .btn--inverse}

## Abstract
Spoken language understanding (SLU) usually requires human semantic annotation on collected data, but the process is expensive. In order to make better use of unlabeled data for robust SLU, we propose an adversarial multi-task learning method by merging a bidirectional language model (BLM) and a slot tagging model (STM). As a secondary objective, the BLM is used to learn generalized and unsupervised knowledge with abundant unlabeled data and improve the performance of STM on unseen data samples. We construct a shared space for both tasks and independent private spaces for each task respectively. Additional adversarial task discriminator is also used to obtain more task-independent sharing information. Experiments show that the proposed approaches achieve the state-of-the-art performance on the small scale ATIS benchmark and significantly improve the semi-supervised performance on a large-scale dataset.

## To cite us
```markdown
@INPROCEEDINGS{lan2018semi,
  author={O. {Lan} and S. {Zhu} and K. {Yu}},
  booktitle={2018 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP)}, 
  title={Semi-Supervised Training Using Adversarial Multi-Task Learning for Spoken Language Understanding}, 
  year={2018},
  volume={},
  number={},
  pages={6049-6053},
}
```