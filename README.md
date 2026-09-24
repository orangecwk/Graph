# Graph-Talker: Hybrid Graph-Embedding Retrieval with Multi-View Graphs for Conversational Speech Synthesis

Authors: Rui Liu, Wenkai Cheng, Zhenqi Jia  
Inner Mongolia University  

---

## Demo Page

[Speech Demo](xxxxxxx)

## 📌 Abstract

Conversational Speech Synthesis (CSS) aims to generate speech with natural prosody and contextually coherent sentiment in multi-turn dialogues, where modeling sentiment dynamics is essential for high-quality generation. Existing approaches predominantly rely on continuous representations of dialogue history, which are inadequate for capturing structured semantic dependencies and fine-grained sentiment evolution, often resulting in structural misalignment between retrieved and current dialogues as well as limited interpretability. To address these challenges, we propose Graph-Talker, a structure-aware retrieval-augmented framework for sentiment-aware CSS. Specifically, we construct hierarchical multi-view dialogue graphs that organize conversations into semantic and sentiment views with global–local structures, and introduce dialogue-level semantic and sentiment captions as global constraint nodes to enhance structured representations. Building upon this, we design a hybrid retrieval strategy that jointly exploits graph structural signals and embedding similarity, along with a hierarchical fusion mechanism that incorporates retrieved knowledge as structural constraints, enabling coordinated modeling of semantic and sentiment information during speech generation. Experimental results demonstrate that Graph-Talker consistently improves sentiment consistency and speech naturalness over strong baselines, while providing an interpretable and extensible framework for structured sentiment modeling in CSS. Code and demos are available at: https://github.com/orangecwk/Graph.

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

* **Dependencies:**
  ```bash
    pip install -r requirements.txt
  ```

