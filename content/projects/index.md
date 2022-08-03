---
date: 2021-08-02T11:04:49+08:00
draft: false
title: Projects
lightgallery: true

math:
  enable: true
---

## Machine Learning Projects

### Sim-to-real via real-to-sim

My dissertation project for Computer Science Masters is a robotics topic on improving the "transfer quality" of policies from the simulations to real-world settings, thereby reducing the *reality gap* induced by the uncertainties and noises in actual environments. A detailed project proposal can be found here: [Dissertation Project Proposal](/files/sim_2_real_proposal.pdf).

As of May 2022, I have completed the project with some minor modifications to the proposed project. Here is [my thesis](/files/Part_III_Dissertation.pdf).

***Abstract***: Data-driven approaches for **multi-robot control problems** have proven very promising with
a variety of model architectures, including deep reinforcement learning, GNN, and Gaussian Processes. So far, simulation data has been the main sampling source, where typically
a large amount of training data is required. The model trained from the simulation, when
deployed onto the real world (**sim-to-real transfer**), can lead to a **significant reality gap**
due to the limitations of simulation assumptions, real-world noises, and robot-robot interactions. Alternatively, we propose that **a direct mapping of current states and reference states to next states can be learnt as the dynamics simulator**, such that the real action policies for different tasks can be learnt with RL methods. We also propose a general framework for such real-world data-driven models on single- and multi-robot systems with an automated and efficient data sampling mechanism.

### Scaffold-based Self-Supervised Learning for Molecular Graphs

This was an independent coursework project for [L45: Representation Learning on Graphs and Networks](https://www.cl.cam.ac.uk/teaching/2122/L45/). The performance of the new approaches presented in this project was rather promising (Read the full paper [here](/files/L45_Project.pdf)). 

***Abstract***: Data augmentation has proven a potent approach for many **self-supervising contrastive learning methods**, where true data can be slightly modified differently into input pairs, such that the model to pre-train can still recognize the original instance after training by matching the representation outputs, making the model robust.
Although such methods have also been applied to graphs with GNN methods, applications on **molecular graphs** in particular requires extra considerations since randomly masking atoms and subgraphs can significantly change the molecular features and will invalidate the augmentation approach. Therefore, we want to
develop a tailored approach for **contrastive learning on molecules**, where **scaffolds** - key structures in molecules that cannot be altered without changing the molecular
properties significantly - are kept intact while we tweak the appended structures
onto them. We will use two main methods for constructing such samples: 1)
**pairing molecules with identical scaffolds as positive samples** and 2) **augmenting each scaffold into a pair of different molecules of the same scaffold backbone.**
We then integrate the augmentation precedures with the GNN model pretraining
and use them for a variety of downstream tasks with different datasets (BBBP,
Freesolv, etc.) for both classification and regression, **benchmarked against random augmentation baselines**. We will also benchmark **various GNNs’ performances** against other non-graph-based models (e.g. SVM, Random Forest) to demonstrate their capability in leveraging the scaffolds.

### Class-Score aggregation vs. Weight-aggregation in Non-iid Federated Learning

I collaborated with *Brady Peng* and *Wanru Zhao* on this Federated Learning project as the final coursework for [L46: Principles of Machine Learning Systems](https://www.cl.cam.ac.uk/teaching/2021/L46/). Our work addressed the non-iid issue faced by many FL systems, where the harm of data heterogeneity can swamp the performance superiority of FL demonstrated on balanced datasets. We tried various popular approaches with some modifications and compared their performances on datasets with a varying degree of heterogeneity. See the full report [here](/files/L46_project.pdf).

***Abstract***: In real-world Federated learning (FL) settings, data distribution among clients is rarely iid. This premise poses a strong challenge to traditional FL approaches. Among many solutions proposed to tackle such data heterogeneity, we provide a straightforward comparison of a few popular approaches, including FedDS and FedPer which use model-weight aggregation, and compare their performance to FedMD which uses class-score aggregation under different degree of non-iid data. In the end, we further expand each of the methods with their own individual experiments and provide a qualitative explanation of their effectiveness.


### PCA-like Autoencoding

In [LE49: Probabilistic Machine Learning](https://www.cl.cam.ac.uk/teaching/2122/LE49/), we covered a wide range of ML topics with the kernel of probabilistic thinking, and I must say I struggled a lot with the course at first. The coursework project, however, provided much clarity for me on interpreting ML algorithms and procedures probabilistically. The central idea behind [this paper](/files/LE49_Project.pdf) may not be as complex as some of my other works, but it offered me tons of insight. 

***Abstract***: Principal Component Analysis(PCA) is a widely popular approach for dimensionality reduction by producing a set of orthogonal latent variables with ordered importance. Autoencoders (AE), which can also be used to learn a predetermined dimension of latent representation, are more capable of capturing complex nonlinear features due to the flexibility of its encoder-decoder architecture. However, importance ordering of latent variables and independence are lost in simple autoencoders, and as such the main objective of this paper is to retain these two features to make it PCA-like while taking advantage of non-linearity from autoencoders. A probabilistic interpretation with variational AE (VAE) is then provided and we integrated the new implementation with two existing methods on a new synthetic dataset ’Rectangles’. We also propose a classification downstream task as a quantitative metric alongside the standard analysis of covariance and interpolations.

### Generative Adversarial Imitation Learning Benchmarking and Investigative Explorations

Based on Reinforcement Learning, imitation learning (IL) loops in an "expert" in the process, where this expert can be either only used for demonstrations as a part of the training data or constantly accessed during training. While behavioral cloning and IRL-RL methods have produced decent results in IL, Generative Adversarial Imitation Learning (GAIL) offered a more flexible and efficient framework for general IL problems, and the [OG paper](https://arxiv.org/abs/1606.03476) established its theoretical foundation. My project, as the core assessment for the course [R255: Advanced Topics in Machine Learning](https://www.cl.cam.ac.uk/teaching/2122/R255/), aimed at reproducing as well as improving on the original GAIL algorithm. While the reproduction results were not as satisfying as expected, some interesting findings can be found [here](/files/R255_zl413_Topic_1.pdf). 

***Abstract***: Generative Adversarial Imitation learning (GAIL), derived from inverse reinforcement learning (IRL), has shown both theoretic soundness and empirical prowess in the selected experiments from the original paper. We set out to reproduce some of the experimental results to reiterate the validity in part as well as to lay out
the caveats in the original conclusions with detailed analysis, since we are unable to recover similar outcomes in some cases. An extension to novel environments was conducted to further test the capabilities of GAIL as opposed to the baseline methods. We also endeavored to improve GAIL performance by adjusting the regularization and architectural hyperparameters. With all the challenges and issues in mind from the experimental and exploratory work, we proposed several valuable research tracks for a more comprehensive future work, training resources permitting.

### Background Matting with Transformers

My very first project in [Computer Lab](https://www.cst.cam.ac.uk/) was the coursework from [L335: Machine Visual Perception](https://www.cl.cam.ac.uk/teaching/2122/L335/). Image/Video Matting, in plain words, refers to obtaining the foreground elements (such as human beings, faces, featured objects, etc.) from the background. While CNN-based approaches have been widely applied to this field, their capabilities of capturing global features on images are lacking compared with transformer-enabled models. Therefore, this project aimed at integrating selected existing CNN backbones with customised transformer blocks and applying the full architecture to image and video matting. Given the short span of the project (less than 3 weeks), some preliminary work and findings can be found in [this report](/files/L335_Report.pdf). 