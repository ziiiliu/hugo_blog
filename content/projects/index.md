---
date: 2021-08-02T11:04:49+08:00
draft: false
title: Projects
lightgallery: true

math:
  enable: true
---

# My Projects

## Sim-to-real via real-to-sim

My dissertation project for Computer Science Masters is a robotics topic on improving the "transfer quality" of policies from the simulations to real-world settings, thereby reducing the *reality gap* induced by the uncertainties and noises in actual environments. A detailed project proposal can be found here: [Dissertation Project Proposal](/files/sim_2_real_proposal.pdf).

As of May 2022, I have completed the project with some minor modifications to the proposed project. Here is [my thesis](/files/Part_III_Dissertation.pdf).

***Abstract***: Data-driven approaches for **multi-robot control problems** have proven very promising with
a variety of model architectures, including deep reinforcement learning, GNN, and Gaussian Processes. So far, simulation data has been the main sampling source, where typically
a large amount of training data is required. The model trained from the simulation, when
deployed onto the real world (**sim-to-real transfer**), can lead to a **significant reality gap**
due to the limitations of simulation assumptions, real-world noises, and robot-robot interactions. Alternatively, we propose that **a direct mapping of current states and reference states to next states can be learnt as the dynamics simulator**, such that the real action policies for different tasks can be learnt with RL methods. We also propose a general framework for such real-world data-driven models on single- and multi-robot systems with an automated and efficient data sampling mechanism.

## Scaffold-based Self-Supervised Learning for Molecular Graphs

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

## Class-Score aggregation vs. Weight-aggregation in Non-iid Federated Learning
