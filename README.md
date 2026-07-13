<div align="center">

# REBASE: Reference-Background Subspace Elimination for Training-Free In-Context Segmentation

[![arXiv](https://img.shields.io/badge/arXiv-2607.09082-b31b1b.svg)](https://arxiv.org/abs/2607.09082v1)

Mantha Sai Gopal, Jaison Saji Chacko, Harsh Nandwana, Sandesh Hegde, Debarshi Banerjee, Uma Mahesh

*CamCom Technologies Private Limited*

</div>

<p align="center">
  <img src="docs/figures/qualitative/coco_grid_top5.png" width="100%">
</p>

Training-free in-context segmentation. A single reference image and its binary mask are sufficient to segment the same category in any query image—no gradient updates or per-target adaptation required.

## Method

<p align="center">
  <img src="docs/figures/preview_method_arch-1.png" width="90%">
</p>

## Results

| Method | ISIC | X-Ray | FSS-1000 | PASCAL-Part | PACO-Part |
|:---|:---:|:---:|:---:|:---:|:---:|
| PerSAM  | 23.9 | 31.7 | 71.2 | 32.5 | 22.5 |
| Matcher | 38.6 | 70.8 | 87.0 | 42.9 | 34.7 |
| GF-SAM  | 48.7 | 51.0 | <ins>88.0</ins> | 44.5 | 36.3 |
| INSID3&nbsp;(DINOv3-L) | <ins>54.4</ins> | 78.8 | 83.7 | **50.5** | <ins>38.7</ins> |
| **REBASE (ours)** | **63.6** | **87.8** | **88.6** | <ins>46.1</ins> | **39.6** |

1-shot mIoU (%, ↑). All training-free methods except INSID3 use DINOv2-L.

## Code

Code release coming soon. ⭐ star the repo for updates.

## Citation

```bibtex
@article{gopal2026rebase,
  title   = {REBASE: Reference-Background Subspace Elimination for Training-Free In-Context Segmentation},
  author  = {Mantha Sai Gopal and Jaison Saji Chacko and Harsh Nandwana and Sandesh Hegde and Debarshi Banerjee and Uma Mahesh},
  journal = {arXiv preprint arXiv:2607.09082},
  year    = {2026}
}
```

## Acknowledgements

Builds on [SAM](https://github.com/facebookresearch/segment-anything) and [DINOv2](https://github.com/facebookresearch/dinov2), and compares against [PerSAM](https://github.com/ZrrSkywalker/Personalize-SAM), [Matcher](https://github.com/aim-uofa/Matcher), [GF-SAM](https://github.com/ANDYZAQ/GF-SAM), and [INSID3](https://github.com/visinf/INSID3).
