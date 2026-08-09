# Data Synthesis

## Overview

Our paper, **“Rethinking Label Consistency of In-Context Learning: An Implicit Transductive Label Propagation Perspective,”** has been accepted to **AAAI 2026**.

📄 **Paper:** [arXiv:2512.12175](https://arxiv.org/pdf/2512.12175)

This repository contains the code for the paper *TopK Sampling with Synthetic Data for In-Context Learning*. Our implementation is based on the OpenICL repository and the `revisit_demon_selection_in_ICL` repository.

The reference works and related projects are as follows:

- [OpenICL: An Open-Source Framework for In-Context Learning](https://arxiv.org/abs/2303.02913)
- [OpenICL GitHub Repository](https://github.com/Shark-NLP/OpenICL)

## Installation

OpenICL requires **Python 3.8 or later**.

For local development, clone this repository and install it in editable mode:

```bash
git clone https://github.com/Cauchy2001/TopK-SD_for_ICL.git
cd TopK-SD_for_ICL
pip install -e .
```

## Examples

The following example demonstrates how to perform in-context learning on a sentiment classification dataset.

Our experiment code is located in the `exp` directory. The main script for the classification experiments is `run_classification.py`.

```bash
cd exp
CUDA_VISIBLE_DEVICES=0 python run_classification.py
```

More examples and tutorials can be found in the [OpenICL examples directory](https://github.com/Shark-NLP/OpenICL/tree/main/examples).

## Citation

If you find this repository useful, please consider citing our paper:

```bibtex
@inproceedings{topksd2026,
  title     = {Rethinking Label Consistency of In-Context Learning:
               An Implicit Transductive Label Propagation Perspective},
  booktitle = {Proceedings of the AAAI Conference on Artificial Intelligence},
  year      = {2026}
}
```

The complete BibTeX entry will be updated when the official proceedings become available.

## Acknowledgements

This project builds upon the OpenICL framework and the `revisit_demon_selection_in_ICL` repository. We sincerely thank the authors and contributors of these projects for making their code publicly available.