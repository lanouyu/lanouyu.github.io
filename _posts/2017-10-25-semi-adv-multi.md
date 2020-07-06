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

## Introduction
Spoken language understanding (SLU) usually requires human semantic annotation on collected data, but the process is expensive. In order to make better use of unlabeled data for robust SLU, we propose an adversarial multi-task learning method by merging a bidirectional language model (BLM) and a slot tagging model (STM). As a secondary objective, the BLM is used to learn generalized and unsupervised knowledge with abundant unlabeled data and improve the performance of STM on unseen data samples. We construct a shared space for both tasks and independent private spaces for each task respectively. Additional adversarial task discriminator is also used to obtain more task-independent sharing information. Experiments show that the proposed approaches achieve the state-of-the-art performance on the small scale ATIS benchmark and significantly improve the semi-supervised performance on a large-scale dataset.

## Method
![method](/assets/images/posts-semi-method.png)

Inspired by the success of shared-private models, we propose an adversarial multi-task learning method for SLU which learns generalized and unsupervised knowledge and regularizes the slot tagging model. The motivation is to tune the slot tagging model by integrating general language information from unlabeled data. Specifically, a bidirectional language model (BLM) and a slot tagging model (STM) are combined by a shared space and two task-specific private spaces. The BLM learns underlying general patterns of semantic and syntactic composition with abundant unsupervised data, while the STM obtains supervised knowledge with limited labeled data. The shared space is trained for both tasks. 

Furthermore, we investigate an adversarial task discriminator as a rival to the shared space. The aim of the task discriminator is to figure out which task are the shared features trained for at each time. In order to confuse the task discriminator, the shared space is forced to extract task-invariant knowledge and jettison task-specific information. The task discriminator is applied on word-level or sentence-level. Unlike Chen et al who trained their models only for Chinese word segmentation task by supervised learning on multiple segmentation criteria with the same data source, we adopt distinctive training objectives, methods and data sources for each task.

![method](/assets/images/posts-semi-algo.png)

## Experiments
The experiments are conducted on the standard ATIS corpus and a large-scale dataset which contains about 30-thousand utterances from three different domains. For the small dataset, the proposed methods obtain the state-of-theart performance compared to published models. For the large dataset, the models are evaluated on semi-supervised learning performance with different amounts of labeled data. The results show that the proposed approaches perform better than
previous methods.

![method](/assets/images/posts-semi-exp-1.png)
![method](/assets/images/posts-semi-exp-2.png)

## To cite us
```markdown
@INPROCEEDINGS{lan2018semi,
  author={O. {Lan} and S. {Zhu} and K. {Yu}},
  booktitle={2018 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP)}, 
  title={Semi-Supervised Training Using Adversarial Multi-Task Learning for Spoken Language Understanding}, 
  year={2018},
  pages={6049-6053},
}
```