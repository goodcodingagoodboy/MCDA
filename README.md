<div align="center">

# MCDA

### Multi-View Graph Contrastive Learning with Dynamic Topology Augmentation for Functional MRI Analysis

[![arXiv](https://img.shields.io/badge/arXiv-2610.26322-b31b1b.svg)](https://arxiv.org/abs/2610.26322)
[![Paper](https://img.shields.io/badge/Paper-Open_Access-4CAF50.svg)](https://arxiv.org/pdf/2610.26322)
[![Code status](https://img.shields.io/badge/Code-In_Preparation-yellow.svg)](#code-release)

**Hao Zhang<sup>1,2</sup>, Xiaoyun Liu<sup>3</sup>, Shuo Huang<sup>2</sup>, Yue Ma<sup>4</sup>, Liang Cao<sup>5</sup>, Mingxia Liu<sup>6</sup>, Li Zhang<sup>2</sup>**

<sup>1</sup> Fudan University &nbsp;&nbsp; <sup>2</sup> Nanjing Forestry University<br>
<sup>3</sup> Southeast University &nbsp;&nbsp; <sup>4</sup> Jiangsu Health Vocational College<br>
<sup>5</sup> Taian Tumor Hospital &nbsp;&nbsp; <sup>6</sup> University of North Carolina at Chapel Hill

**arXiv preprint · October 2026**

[Paper](https://arxiv.org/abs/2610.26322) · [PDF](https://arxiv.org/pdf/2610.26322) · [Citation](#citation)

<p align="center">
  <a href="img/framework.webp">
    <img src="img/framework.webp" alt="Overview of the MCDA framework, including brain network construction, complementary topology augmentation, dynamic augmentation updates, and multi-view contrastive learning." width="100%">
  </a>
</p>

<p align="center"><em>Overview of the proposed MCDA framework.</em></p>

## Overview

<p align="center">
<strong>MCDA</strong> is a topology-guided multi-view graph contrastive learning framework for resting-state functional MRI (rs-fMRI) analysis and brain disorder identification. It combines <strong>self-aware</strong> and <strong>cross-sample</strong> brain network augmentations with history-guided refinement, learning from subject-specific functional patterns and inter-subject variability.
</p>

<p align="center">
The framework jointly optimizes diagnostic classification and multi-view contrastive learning. The original and two augmented views share a classification branch, and their predicted patient probabilities are averaged during both training and testing.
</p>

<p align="center">
Experiments cover <strong>REST-MDD</strong> and <strong>ABIDE</strong>, with <strong>1,236 subjects</strong> in total. The paper also analyzes the similarity-score optimization directions and a lower bound of the contrastive objective.
</p>

## Dynamic Augmentation Update (DAU) Module

<p align="center">
DAU summarizes recent augmentation histories with a <strong>shared BiGRU</strong> and generates element-wise gates to blend each current augmented view with its branch-specific historical reference.
</p>

<p align="center">
  <a href="img/DAU_Module.png">
    <img src="img/DAU_Module.png" alt="DAU module: graph projection and history windows, shared BiGRU and gate generation, and gated historical fusion." width="100%">
  </a>
</p>

<p align="center"><em>Graph projection and history windows, shared BiGRU encoding, and gated historical fusion.</em></p>

## Exploratory Analysis of Brain Region-Level Associations

<p align="center">
We explore model-derived brain region associations for <strong>MDD vs. HC</strong> on REST-MDD and <strong>ASD vs. HC</strong> on ABIDE. The selected connectivity patterns provide exploratory anatomical context for the learned brain network representations.
</p>

<p align="center">
  <a href="img/Discriminative_FCs.jpg">
    <img src="img/Discriminative_FCs.jpg" alt="Selected brain region associations shown from multiple anatomical views: MDD versus healthy controls on the left and ASD versus healthy controls on the right." width="100%">
  </a>
</p>

<p align="center"><em>Selected brain region associations for (a) MDD vs. HC and (b) ASD vs. HC.</em></p>

## Code Release

<p align="center">
The implementation is being organized for a structured public release. Setup instructions, dependencies, and training and evaluation commands will accompany the code release.
</p>

## To-do List

<p align="center">
☑ Release the paper on arXiv.<br>
☑ Add paper information, the framework, and module illustrations.<br>
☐ Organize, clean, and release the source code.<br>
☐ Add environment setup and dependency requirements.<br>
☐ Add data preparation, training, and evaluation instructions.
</p>

## Citation

<p align="center">If you find this work useful, please cite:</p>

<details>
<summary><strong>BibTeX</strong></summary>

```bibtex
@misc{zhang2026mcda,
  title         = {{MCDA}: Multi-View Graph Contrastive Learning with Dynamic Topology Augmentation for Functional {MRI} Analysis},
  author        = {Hao Zhang and Xiaoyun Liu and Shuo Huang and Yue Ma and Liang Cao and Mingxia Liu and Li Zhang},
  year          = {2026},
  eprint        = {2610.26322},
  archivePrefix = {arXiv},
  url           = {https://arxiv.org/abs/2610.26322}
}
```

</details>

</div>
