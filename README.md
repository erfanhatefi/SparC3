<div align="center">
  <img src="/docs/source/static/logo.svg" width="400"/><br><br>
  <img src="/docs/source/static/paper_title.svg" width="600"/>
</div>

[![arXiv](https://img.shields.io/badge/arXiv-2506.13727-b31b1b.svg)](https://arxiv.org/abs/2506.13727)

---

## Overview

This repository contains the implementation of **SparC³**, a novel framework for pruning Large Language Models (LLMs) that leverages **Layer-wise Relevance Propagation (LRP)**. It supports three key applications:


- **Compression**: Unstructured pruning of LLMs with minimal performance loss
- **Circuit Discovery**: Extraction of task-relevant subgraphs (circuits)
- **Targeted Model Correction**: Removal of circuits responsible for spurious behaviors

## 🚧 Work in Progress

This repository is currently under development. The code will be published soon. Please stay tuned for updates!

---

## Abstract

Large Language Models (LLMs) are widely deployed in real-world applications, yet their internal mechanisms remain difficult to interpret and control, limiting our ability to diagnose and correct undesirable behaviors. Mechanistic interpretability addresses this challenge by identifying circuits - subsets of model components responsible for specific behaviors. However, discovering such circuits in LLMs remains difficult due to their scale and complexity. We frame circuit discovery as identifying parameters that contribute most to model outputs on task-specific inputs, and use Layer-wise Relevance Propagation (LRP) with reference samples to attribute and extract these components via pruning. Building on this, we introduce contrastive relevance to isolate circuits associated with undesired behaviors while preserving general capabilities, enabling targeted model correction. On OPT-125M, we show that pruning as little as ~0.3% of neurons substantially reduces toxic outputs, while pruning approximately 0.03% of weight elements mitigates repetitive text generation without degrading general performance. These results establish attribution-guided pruning as an effective mechanism for identifying and intervening on behavior-specific circuits in LLMs. We further validate our findings on additional small-scale language models, demonstrating that the proposed approach transfers across architectures.

<div align="center">
  <img src="/docs/source/static/intro_story.png" width="1000"/>
  <p>Attribution-guided Pruning for <span style="color: #C23F40;">C</span>ompression, <span style="color: #2EA02C;">C</span>ircuit Discovery, and <span style="color: #E6AC00;">C</span>orrection in LLMs</p>
</div>

---
## Citation

If you find this work useful, please cite our paper:

```bibtex
@misc{atefi2026attributionguidedpruninginsightcontrol,
      title={Attribution-Guided Pruning for Insight and Control: Circuit Discovery and Targeted Correction in Small-scale LLMs}, 
      author={Sayed Mohammad Vakilzadeh Hatefi and Maximilian Dreyer and Reduan Achtibat and Patrick Kahardipraja and Thomas Wiegand and Wojciech Samek and Alexander Binder and Sebastian Lapuschkin},
      year={2025},
      eprint={2506.13727},
      url={https://arxiv.org/abs/2506.13727}, 
}
```

