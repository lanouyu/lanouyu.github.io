---
title: "AlpacaTag: An Active Learning-based Crowd Annotation Framework for Sequence Tagging"
read_time: false
toc: true
tags:
  - Natural Language Processing
  - Crowd Annotaions
---

Bill Yuchen Lin, Dong-Ho Lee, Frank F Xu, Ouyu Lan, and Xiang Ren

*ACL Demo, 2019*

[Paper](https://www.aclweb.org/anthology/P19-3010.pdf){: .btn .btn--inverse}
[Code](https://inklab.usc.edu/AlpacaTag/){: .btn .btn--inverse}
[Poster](https://inklab.usc.edu/AlpacaTag/poster.pdf){: .btn .btn--inverse}

## Introduction
We introduce an open-source web-based data annotation framework (AlpacaTag) for sequence tagging tasks such as named-entity recognition (NER). The distinctive advantages of AlpacaTag are three-fold. 
* Active intelligent recommendation: dynamically suggesting annotations and sampling the most informative unlabeled instances with a back-end active learned model; 
* Automatic crowd consolidation: enhancing real-time inter-annotator agreement by merging inconsistent labels from multiple annotators; 
* Real-time model deployment: users can deploy their models in downstream systems while new annotations are being made. 

AlpacaTag is a comprehensive solution for sequence labeling tasks, ranging from rapid tagging with recommendations powered by active learning and auto-consolidation of crowd annotations to real-time model deployment.

## Method
![method](/assets/images/posts-alpaca-method.png)

As shown in the figure, AlpacaTag has an actively learned back-end model (top-left) in addition to a front-end web-UI (bottom). Thus, we have two separate servers: a back-end model server and a front-end annotation server. The model server is built with PyTorch and supports a set of APIs for communications between the two servers and model deployment. The annotation server is built on Django in Python, which interacts with administrators and annotators.

## Experiments
![method](/assets/images/posts-alpaca-exp-1.png)

As shown in the figure, the performance with active
learning is indeed improved by a large margin over
vanilla training effectively.

![method](/assets/images/posts-alpaca-exp-2.png)

As shown in the table, our
methods outperform existing approaches including MVT-SLM (Wang et al., 2018) and CrowdX (Nguyen et al., 2017).

## To cite us
```markdown
@InProceedings{
  bill2019alpaca,
  author = {Bill Yuchen Lin and Dongho Lee and Frank F. Xu and Ouyu Lan and Xiang Ren},
  title = {AlpacaTag: An Active Learning-based Crowd Annotation Framework for Sequence Tagging. },
  booktitle = {Proceedings of the 57th Annual Meeting of the Association for Computational Linguistics (Demo Track)},
  year = {2019},
  pages = {58-63},
}
```