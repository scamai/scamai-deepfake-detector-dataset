# scamai-deepfake-detector-dataset
This repository contains the dataset used in the research paper 'Do Deepfake Detectors Work in Reality?', done by Scam AI.

# Real-World Faceswap Dataset (RWFS)

<div align="center">

![Scam.ai Logo](https://img.shields.io/badge/Scam.ai-Research-blue)
[![Dataset Downloads](https://img.shields.io/github/downloads/scam-ai/scamai-deepfake-detector-dataset/total?color=green&label=Dataset%20Downloads)](https://github.com/scam-ai/scamai-deepfake-detector-dataset/releases)
[![Paper](https://img.shields.io/badge/Paper-arXiv:2502.10920-red)](https://arxiv.org/abs/2502.10920)
[![GitHub stars](https://img.shields.io/github/stars/scam-ai/scamai-deepfake-detector-dataset?style=social)](https://github.com/scam-ai/scamai-deepfake-detector-dataset/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/scam-ai/scamai-deepfake-detector-dataset?style=social)](https://github.com/scam-ai/scamai-deepfake-detector-dataset/network/members)
![Visitors](https://visitor-badge.laobi.icu/badge?page_id=scam-ai.scamai-deepfake-detector-dataset)

</div>

## Overview

This repository contains the Real-World Faceswap Dataset (RWFS) used in our research paper ["Do Deepfake Detectors Work in Reality?"](https://arxiv.org/abs/2502.10920). RWFS is the first dataset specifically designed to reflect real-world deepfakes as they appear in the wild, rather than in controlled academic environments.

## Key Findings

- Current state-of-the-art deepfake detectors perform poorly on real-world deepfakes
- Super-resolution post-processing significantly degrades detector performance
- The performance gap between academic and real-world scenarios is substantial
- Deepfake detectors trained on academic datasets approach random guessing on real-world samples

## Dataset Description

The RWFS dataset contains:
- 847 real-world deepfake images from 8 popular online faceswap tools
- 900 real images from the Celeb dataset as authentic samples
- All images follow race-gender-age matching to create realistic swaps

### Source Breakdown

| Source Website | Number of Images |
|----------------|------------------|
| Pixlr | 81 |
| Magic Hour | 104 |
| Remaker | 92 |
| AI FaceSwap IO | 71 |
| Ismarta | 93 |
| Pica | 84 |
| Vidwud | 95 |
| Faceswapper | 227 |
| **Total** | **847** |

## Usage

```python
# Example code to load and use the dataset
import os
import cv2
import numpy as np

# Load real images
real_path = "./rwfs_dataset/real/"
real_images = [cv2.imread(os.path.join(real_path, f)) for f in os.listdir(real_path)]

# Load fake images
fake_path = "./rwfs_dataset/fake/"
fake_images = [cv2.imread(os.path.join(fake_path, f)) for f in os.listdir(fake_path)]

# Use for training/evaluating deepfake detectors
```

## Citation

If you use this dataset in your research, please cite our paper:

```bibtex
@article{ren2025do,
  title={Do Deepfake Detectors Work in Reality?},
  author={Ren, Simiao and Xu, Hengwei and Ng, Tsang and Zewde, Kidus and Jiang, Shengkai and Desai, Ramini and Patil, Disha and Cheng, Ning-Yau and Zhou, Yining and Muthukrishnan, Ragavi},
  journal={arXiv preprint arXiv:2502.10920},
  year={2025}
}
```

## Dataset Statistics and Impact

<div align="center">
  
[![Dataset Usage](https://img.shields.io/badge/dynamic/json?color=blue&label=Dataset%20Usage&query=$.count&url=https://api.github.com/repos/scam-ai/scamai-deepfake-detector-dataset/releases)](https://github.com/scam-ai/scamai-deepfake-detector-dataset/releases)
[![Research Citations](https://img.shields.io/badge/dynamic/json?color=orange&label=Citations&query=$.citation_count&url=https://api.semanticscholar.org/graph/v1/paper/arXiv:2502.10920)](https://www.semanticscholar.org/paper/Do-Deepfake-Detectors-Work-in-Reality-Ren-Xu/ae3c7f1fb9df4b2f8e47a9c2bddce1a1a9f1f9a9)

</div>

## Key Contributions

1. **First Real-World Faceswap Dataset**: Hand-collected from top-ranked online faceswap tools
2. **Benchmarking of SOTA Detectors**: Evaluation of current deepfake detection methods
3. **Super-Resolution Impact**: Discovery of how post-processing undermines detectors
4. **Quantitative Analysis**: Detailed analysis of deepfake detector performance degradation

## License

This dataset is released under the [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/).

## Contact

For questions about the dataset or research paper, please contact:
- Simiao Ren: simiao.ren@duke.edu
- General inquiries: research@scam.ai

---

<div align="center">
  <a href="https://scam.ai">
    <img src="https://img.shields.io/badge/Scam.ai-Website-blue" alt="Scam.ai Website">
  </a>
</div>