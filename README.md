# [Journal of Web Engineering] Personalized User Models in a Real-world Edge Computing Environment: A Peer-to-peer Federated Learning Framework

Detailed information for [Personalized User Models in a Real-world Edge Computing Environment: A Peer-to-peer Federated Learning Framework](https://journals.riverpublishers.com/index.php/JWE/article/view/28237) by *Xiangchi Song, Zhaoyan Wang, KyeongDeok Baek*, and *In-Young Ko*. School of Computing,  Korea Advanced Institute of Science and Technology,  Daejeon, Republic of Korea. This is the extended version of paper [EPFLU: Efficient Peer-to-peer Federated Learning for Personalized User Models in Edge-Cloud Environments](https://link.springer.com/chapter/10.1007/978-3-031-75110-3_1) published in ICWE 2024, most of the basic settings are the same, only the updates are introduced here.

## Table of Contents
* Overview
* Experimental Setup Based on Real-world Server Distribution
* Code & Experimental Records
* Contact
* Special Thanks
* References


## Overview

As the number of IoT devices and the volume of data increase, distributed computing systems have become the primary deployment solution for largescale Internet of Things (IoT) environments. Federated learning (FL) is a collaborative machine learning framework that allows for model training using data from all participants while protecting their privacy. However, traditional FL suffers from low computational and communication efficiency in large-scale hierarchical cloud-edge collaborative IoT systems. Additionally, due to heterogeneity issues, not all IoT devices necessarily benefit from the global model of traditional FL, but instead require the maintenance of personalized levels in the global training process. Therefore we extend FL into a horizontal peer-to-peer (P2P) structure and introduce our P2PFL framework: efficient peer-to-peer federated learning for users (EPFLU). EPFLU transitions the paradigms from vertical FL to a horizontal P2P structure from the user perspective and incorporates personalized enhancement techniques using private information. Through horizontal consensus information aggregation and private information supplementation, EPFLU solves the weakness of traditional FL that dilutes the characteristics of individual client data and leads to model deviation. This structural transformation also significantly alleviates the original communication issues. Additionally, EPFLU has a customized simulation evaluation framework, and uses the EUA dataset containing real-world edge server distribution, making it more suitable for real-world large-scale IoT. Within this framework, we design two extreme data distribution scenarios and conduct detailed experiments of EPFLU and selected baselines on the MNIST and CIFAR-10 datasets. The results demonstrate that the robust and adaptive EPFLU framework can consistently converge to optimal performance even under challenging data distribution scenarios. Compared with the traditional FL and selected P2PFL methods, EPFLU achieves communication time improvements of 39% and 16% respectively.

## Experimental Setup Based on Real-world Server Distribution
<div align=center>
<img src="https://github.com/XiangchiSong/JWE_EPFLU/blob/main/Figures/EUA.png" alt="Image" width="600">
</div>

We utilized a set of [EUA datasets](https://github.com/PhuLai/eua-dataset) derived from real-world data sources[1], which includes the geographical locations of all cellular base stations in Australia. In our study, we used the server distribution data from the dataset and subsequently deployed the data and models at these server locations.

Geographical Range:
- **Latitude Range**: `[-33.5, -33]`.
- **Longitude Range**: `[140, 150]`.

Sampling Settings:
- **Client Nodes**: `664`.
- **Client Nodes**: `500`.

It is a reasonable sampling range that prevents issues resulting from a region that is too large, which could cause excessive distances between some clients, and from a region that is too small, which could lead to redundant sampling. It is important to note that the EUA dataset itself does not distinguish between cloud and edge servers. In traditional FL methods, the cloud server’s role is to be the aggregator, aggregating submodels from clients. Therefore, we selected the server closest to the center of this range as the aggregator. We assume this server does not participate in training but only in the aggregation process, acting as the cloud server for selected FL algorithms.

## Code & Experimental Records
***We will make it public after the paper is published.***

## Contact
If you like our works, please cite our paper:

```
@article{song2024personalized,
  title={Personalized User Models in a Real-world Edge Computing Environment: A Peer-to-peer Federated Learning Framework},
  author={Song, Xiangchi and Wang, Zhaoyan and Baek, KyeongDeok and Ko, In-Young},
  journal={Journal of Web Engineering},
  pages={1057--1084},
  year={2024}
}
```

Also, feel free to contact us: xcsong@kaist.ac.kr, we will reply to you within three working days！

## Special Thanks
We would like to give a special thanks to the friends who provided help in this paper. We thank [Tuo Zhang](https://tuo-zhang.com/) for inspiring our research ideas, [Qian Chen](https://kqkq926.github.io/) for providing us with the baseline reproduction method[2], and [Jed Mills](https://scholar.google.com/citations?user=30_1nBcAAAAJ&hl=zh-CN&oi=sra)'s work for inspiring our personalized solution[3].

## References
[1] Phu Lai, Qiang He, Mohamed Abdelrazek, Feifei Chen, John Hosking, John Grundy, and Yun Yang, [Optimal Edge User Allocation in Edge Computing with Variable Sized Vector Bin Packing](https://link.springer.com/chapter/10.1007/978-3-030-03596-9_15), 16th International Conference on Service-Oriented Computing (ICSOC2018), pp. 230-245, Hangzhou, China, 2018.

[2] Chen Q, Wang Z, Zhang W, et al. [PPT: A privacy-preserving global model training protocol for federated learning in P2P networks](https://www.sciencedirect.com/science/article/pii/S0167404822003583)[J]. Computers & Security, 2023, 124: 102966.

[3] Mills J, Hu J, Min G. [Multi-task federated learning for personalised deep neural networks in edge computing](https://ieeexplore.ieee.org/abstract/document/9492755)[J]. IEEE Transactions on Parallel and Distributed Systems, 2021, 33(3): 630-641.

## 
Copyright © 2024 Xiangchi Song, Zhaoyan Wang, KyeongDeok Baek, and In-Young Ko

This research was partly supported by the MSIT (Ministry of Science and ICT), Korea, under the ITRC (Information Technology Research Center) support program (IITP-2024-2020-0-01795) supervised by the IITP (Institute for Information & Communications Technology Planning & Evaluation) and IITP grant funded by the Korea government (MSIT) (No. RS-2024-00406245, Development of Software-Defined Infrastructure Technologies for Future Mobility).

All rights reserved. No part of this publication may be reproduced, distributed, or transmitted in any form or by any means, including photocopying, recording, or other electronic or mechanical methods, without the prior written permission of the publisher, except in the case of brief quotations embodied in critical reviews and certain other noncommercial uses permitted by copyright law. For permission requests, please email to the author.
