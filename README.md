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

Large Language Models (LLMs) are central to many contemporary AI applications, yet their extensive parameter counts pose significant challenges for deployment in memory- and compute-constrained environments. Recent works in eXplainable AI (XAI), particularly on attribution methods, suggest that interpretability can also enable model compression by identifying and removing components irrelevant to inference. In this paper, we leverage Layer-wise Relevance Propagation (LRP) to perform attribution-guided pruning of LLMs. While LRP has shown promise in structured pruning for vision models, we extend it to unstructured pruning in LLMs and demonstrate that it can substantially reduce model size with minimal performance loss. Our method is especially effective in extracting task-relevant subgraphs -- so-called ``circuits'' -- which can represent core functions (e.g., indirect object identification). Building on this, we introduce a technique for model correction, by selectively removing circuits responsible for spurious behaviors (e.g., toxic outputs). All in all, we gather these techniques as a uniform holistic framework and showcase its effectiveness and limitations through extensive experiments for compression, circuit discovery and model correction on Llama and OPT models, highlighting its potential for improving both model efficiency and safety.

<div align="center">
  <img src="/docs/source/static/intro_story.png" width="1000"/>
  <p>Attribution-guided Pruning for <span style="color: #C23F40;">C</span>ompression, <span style="color: #2EA02C;">C</span>ircuit Discovery, and <span style="color: #E6AC00;">C</span>orrection in LLMs</p>
</div>

---
## Citation

If you find this work useful, please cite our paper:

```bibtex
@misc{hatefi2025attributionguidedpruningcompressioncircuit,
      title={Attribution-guided Pruning for Compression, Circuit Discovery, and Targeted Correction in LLMs}, 
      author={Sayed Mohammad Vakilzadeh Hatefi and Maximilian Dreyer and Reduan Achtibat and Patrick Kahardipraja and Thomas Wiegand and Wojciech Samek and Sebastian Lapuschkin},
      year={2025},
      eprint={2506.13727},
      url={https://arxiv.org/abs/2506.13727}, 
}
```

