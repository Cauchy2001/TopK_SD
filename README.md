# TopK-SD: Rethinking Label Consistency of In-Context Learning

> **An Implicit Transductive Label Propagation Perspective**  
> *Accepted to the Fortieth AAAI Conference on Artificial Intelligence (AAAI 2026)*

This repository contains the official implementation of our paper **“Rethinking Label Consistency of In-Context Learning: An Implicit Transductive Label Propagation Perspective,”** accepted to the **Fortieth AAAI Conference on Artificial Intelligence (AAAI 2026)**.

---

## 📝 Paper

**Title:** Rethinking Label Consistency of In-Context Learning: An Implicit Transductive Label Propagation Perspective

**Authors:** Haoyang Chen, Richong Zhang\*, Junfan Chen

\* Corresponding author.

**Affiliations:**

- School of Software, Beihang University, Beijing, China
- CCSE, School of Computer Science and Engineering, Beihang University, Beijing, China
- Zhongguancun Laboratory, Beijing, China

**Conference:** The Fortieth AAAI Conference on Artificial Intelligence (AAAI 2026)

**Organizer:** Association for the Advancement of Artificial Intelligence (AAAI)

**Links:**

- 📄 [arXiv Paper](https://arxiv.org/pdf/2512.12175)
- 🔗 [AAAI Official](https://doi.org/10.1609/aaai.v40i36.40273)
- 💻 [Code Repository](https://github.com/Cauchy2001/TopK-SD)

---

## 🎯 Abstract

Large language models (LLMs) perform in-context learning (ICL) with minimal supervised examples, benefiting various natural language processing tasks. One critical research focus is the selection of prompt demonstrations. Current approaches typically employ retrieval models to select the top-*K* most semantically similar examples as demonstrations.

However, we argue that existing methods are limited since **label consistency is not guaranteed** during demonstration selection. Our cognition derives from the Bayesian view of ICL and our rethinking of ICL from the **transductive label propagation perspective**. We treat ICL as a transductive learning method and incorporate latent concepts from the Bayesian view, deducing that similar demonstrations guide the concepts of the query, with consistent labels serving as estimates.

Based on this understanding, we establish a **label propagation framework** to link label consistency with propagation error bounds. To model label consistency, we propose a **data synthesis method** that leverages both semantic and label information and use **TopK Sampling with Synthetic Data (TopK-SD)** to acquire demonstrations with consistent labels.

---

## ✨ Key Contributions

1. **New Perspective:** We rethink ICL from an implicit transductive label propagation perspective, providing a theoretical foundation for understanding demonstration selection.

2. **Label Propagation Framework:** We establish a theoretical framework linking label consistency with propagation error bounds.

3. **TopK-SD Method:** We propose a data synthesis approach that leverages both semantic and label information to select demonstrations with consistent labels.

4. **SOTA Performance:** TopK-SD outperforms the original TopK sampling method on multiple benchmarks.

---

## 📊 Key Results

| Setting            | Accuracy | Label Consistency |
| ------------------ | -------- | ----------------- |
| Random Selection   | 25%      | ❌ Low            |
| **TopK-SD (Ours)** | **75%**  | ✅ High            |

*On SST-2, for a query with the label “positive,” our method selects demonstrations with the same label to improve ICL performance.*

---

## 🚀 Method Overview

TopK-SD selects in-context demonstrations by:

1. **Synthesizing data** that captures both semantic and label information
2. **Sampling top-K examples** with consistent labels
3. **Improving ICL performance** through better label consistency

---

## 📂 Repository Structure

```text
TopK-SD/
├── exp/
│   └── run_classification.py
├── openicl/
├── requirements.txt
├── setup.py
└── README.md
```

The main experimental code is located in the `exp` directory. The `run_classification.py` script is used to conduct text classification experiments.

---

## 🔧 Installation

OpenICL requires **Python 3.8 or later**.

Clone this repository and install the package in editable mode:

```bash
git clone https://github.com/Cauchy2001/TopK-SD.git
cd TopK-SD
pip install -e .
```

---

## ▶️ Examples

The following example demonstrates how to perform in-context learning on a sentiment classification dataset.

Our experimental code is located in the `exp` directory, and `run_classification.py` is the main script for the classification experiments.

```bash
cd exp
CUDA_VISIBLE_DEVICES=0 python run_classification.py
```

More examples and tutorials for the underlying OpenICL framework can be found in the [OpenICL examples directory](https://github.com/Shark-NLP/OpenICL/tree/main/examples).

---

## 🙏 Acknowledgements

Our implementation is based on the following open-source projects:

- [OpenICL: An Open-Source Framework for In-Context Learning](https://github.com/Shark-NLP/OpenICL)
- `revisit_demon_selection_in_ICL`

We sincerely thank the authors and contributors of these projects for making their code publicly available.

---

## 📖 Citation

If you find this work useful, please cite our paper:

```bibtex
@inproceedings{chen2026rethinking,
  title     = {Rethinking Label Consistency of In-Context Learning:
               An Implicit Transductive Label Propagation Perspective},
  author    = {Chen, Haoyang and Zhang, Richong and Chen, Junfan},
  booktitle = {Proceedings of the Fortieth AAAI Conference on Artificial Intelligence},
  year      = {2026},
  doi       = {10.1609/aaai.v40i36.40273}
}
```