# Graph-Talker: Hybrid Graph-Embedding Retrieval with Multi-View Graphs for Conversational Speech Synthesis


[![Demo Page](https://img.shields.io/badge/Web-Demo%20Page-blue.svg)](https://anonymous.4open.science/r/GraphTalker)

This repository contains the official PyTorch implementation of the paper:
**"HYBRID GRAPH-EMBEDDING RETRIEVAL WITH MULTI-VIEW GRAPHS FOR CONVERSATIONAL SPEECH SYNTHESIS"**.

> **Authors:** Rui Liu*, Wenkai Cheng, Zhenqi Jia  
> **Affiliation:** Inner Mongolia University  
> **Demo Page:** [Graph-Talker Audio Demos](https://anonymous.4open.science/r/GraphTalker)

---

## 📌 Abstract

Conversational Speech Synthesis (CSS) aims to generate speech with natural prosody and contextually coherent sentiment in multi-turn dialogues. Existing methods struggle to capture structured semantic dependencies and fine-grained sentiment evolution across dialogue instances. 

To address these challenges, we propose **Graph-Talker**, a structure-aware retrieval-augmented framework for sentiment-aware CSS:
1. **Multi-View Hierarchical Graph Construction:** We organize multi-turn conversations into complementary **semantic** and **sentiment** views, anchored by LLM-generated (LLaMA3-8B) global dialogue captions.
2. **Hybrid Graph-Embedding Retrieval:** We design a joint retrieval strategy combining discrete type-constrained **VF2 subgraph matching** (for topological structural similarity) and **continuous embedding similarity**.
3. **Hierarchical Knowledge Fusion:** The retrieved multi-view structural knowledge is hierarchically fused into the acoustic module via cross-attention to guide sentiment-consistent and prosodically coherent speech synthesis.

---

## 🏗️ Model Architecture


1. **Stage 1 (Graph Construction):** Multi-view global-local hierarchical graphs ($G^{(Sem)}$ and $G^{(Sen)}$) are built using text, speaker, acoustic, and emotion attributes along with global caption nodes.
2. **Stage 2 (Hybrid Retrieval):** Coarse pre-filtering via continuous embedding similarity followed by fine-grained topological matching via type-constrained VF2.
3. **Stage 3 & 4 (Fusion & Generation):** Hierarchical cross-graph fusion conditions the acoustic decoder and vocoder (HiFi-GAN) to synthesize speech.

---

## ⚙️ Dependencies and Environment

* **Operating System:** Ubuntu 22.04 LTS
* **Python:** 3.9.18
* **PyTorch:** 2.0.1 + CUDA 11.8
* **Dependencies:**
  ```bash
  pip install -r requirements.txt
```
