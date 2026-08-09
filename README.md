# TopK-SD: Rethinking Label Consistency of In-Context Learning

> **An Implicit Transductive Label Propagation Perspective**  
> *Accepted to AAAI 2026*

This repository contains the official implementation of our paper **"Rethinking Label Consistency of In-Context Learning: An Implicit Transductive Label Propagation Perspective"**, accepted to the **Fortieth AAAI Conference on Artificial Intelligence (AAAI 2026)**.

---

## 📝 Paper

**Title:** Rethinking Label Consistency of In-Context Learning: An Implicit Transductive Label Propagation Perspective

**Authors:** Haoyang Chen, Richong Zhang *, Junfan Chen

**Affiliations:**
- School of Software, Beihang University, Beijing, China
- CCSE, School of Computer Science and Engineering, Beihang University, Beijing, China
- Zhongguancun Laboratory, Beijing, China

**Conference:** AAAI 2026 (Fortieth AAAI Conference on Artificial Intelligence)

**Links:**
- 📄 [arXiv Paper](https://arxiv.org/pdf/2512.12175)
- 🔗 [AAAI Official](https://doi.org/10.1609/aaai.v40i36.40273)
- 💻 [Code Repository](https://github.com/Cauchy2001/TopK-SD)

---

## 🎯 Abstract

Large language models (LLMs) perform in-context learning (ICL) with minimal supervised examples, benefiting various natural language processing tasks. One critical research focus is the selection of prompt demonstrations. Current approaches typically employ retrieval models to select the top-*K* most semantically similar examples as demonstrations.

However, we argue that existing methods are limited since **label consistency is not guaranteed** during demonstration selection. Our cognition derives from the Bayesian view of ICL and our rethinking of ICL from the **transductive label propagation perspective**. We treat ICL as a transductive learning method and incorporate latent concepts from Bayesian view, deducing that similar demonstrations guide the concepts of query, with consistent labels serving as estimates.

Based on this understanding, we establish a **label propagation framework** to link label consistency with propagation error bounds. To model label consistency, we propose a **data synthesis method**, leveraging both semantic and label information, and use **TopK Sampling with Synthetic Data (TopK-SD)** to acquire demonstrations with consistent labels.

---

## ✨ Key Contributions

1. **New Perspective:** Rethinking ICL from an implicit transductive label propagation perspective, providing a theoretical foundation for understanding demonstration selection.

2. **Label Propagation Framework:** Establishes a theoretical framework linking label consistency with propagation error bounds.

3. **TopK-SD Method:** Proposes a data synthesis approach leveraging both semantic and label information to select demonstrations with consistent labels.

4. **SOTA Performance:** TopK-SD outperforms original TopK sampling on multiple benchmarks.

---

## 📊 Key Results

| Setting | Accuracy | Label Consistency |
|---------|----------|-------------------|
| Random Selection | 25% | ❌ Low |
| **TopK-SD (Ours)** | **75%** | ✅ High |

*On SST-2, for a query with the label "positive", our method selects demonstrations with the same label to improve ICL performance.*

---

## 🚀 Method Overview

TopK-SD selects in-context demonstrations by:

1. **Synthesizing data** that captures both semantic and label information
2. **Sampling top-K** examples with consistent labels
3. **Improving ICL performance** through better label consistency

---

## 📄 License

Copyright © 2026, Association for the Advancement of Artificial Intelligence (www.aaai.org). All rights reserved.

---

## 📬 Contact

- **Haoyang Chen:** Cauchy20011214@buaa.edu.cn
- **Richong Zhang:** zhangrc@act.buaa.edu.cn
- **Junfan Chen:** chenjf@act.buaa.edu.cn

---

## 📖 Citation

If you find this work useful for your research, please cite:

```bibtex
@inproceedings{chen2026rethinking,
  title={Rethinking Label Consistency of In-Context Learning: An Implicit Transductive Label Propagation Perspective},
  author={Chen, Haoyang and Zhang, Richong and Chen, Junfan},
  booktitle={Proceedings of the AAAI Conference on Artificial Intelligence},
  volume={40},
  number={36},
  pages={30226--30234},
  year={2026}
}
