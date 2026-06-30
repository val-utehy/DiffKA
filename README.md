<div align="center">



### Diffusion-Guided Knowledge Absorption for Robust Object Detection under Rainy Night Conditions

<p align="center">
  <img src="DiffKA.png" width="90%"><br>
  <b>DiffKA Architecture</b>
</p>

</div>

---

## Introduction

DiffKA is a novel approach for robust object detection under rainy nighttime weather conditions. The model leverages a diffusion-based knowledge absorption mechanism that enables the detector to effectively learn clean features from degraded images. Comprehensive evaluations on various datasets demonstrate that DiffKA acquires the highest performance, outperforming existing methods on two benchmark datasets, including a rainy nighttime (RNT) dataset and a Rain in Driving (RID) dataset. You can download the paper at: Link

---

## Datasets

### RNT dataset: using for training and testing

- **Paper:** [Multilevel knowledge transmission for object detection in rainy night weather conditions (IEEE Transactions on Industrial Informatics 2024)](https://ieeexplore.ieee.org/abstract/document/10541873)
- Dataset split: was kept as original paper. You can download our split files from [Google Drive](https://drive.google.com/drive/folders/1P3Fv2HuSNkagh4i6CMr07T0kcc3jIef8?usp=sharing)

### RID dataset: using for testing only

- **Link:** [Single Image Deraining: A Comprehensive Benchmark Analysis (CVPR 2019)](https://openaccess.thecvf.com/content_CVPR_2019/html/Li_Single_Image_Deraining_A_Comprehensive_Benchmark_Analysis_CVPR_2019_paper.html)

---
## Implementation details
- **Object detection methods (was kept as original paper)**: [RetinaNet](https://openaccess.thecvf.com/content_ICCV_2017/papers/Lin_Focal_Loss_for_ICCV_2017_paper.pdf), [YOLOv4](https://arxiv.org/pdf/2004.10934), [YOLOv7](https://openaccess.thecvf.com/content/CVPR2023/papers/Wang_YOLOv7_Trainable_Bag-of-Freebies_Sets_New_State-of-the-Art_for_Real-Time_Object_Detectors_CVPR_2023_paper.pdf), [YOLOv9](https://link.springer.com/chapter/10.1007/978-3-031-72751-1_1), [YOLOv10](https://proceedings.neurips.cc/paper_files/paper/2024/file/c34ddd05eb089991f06f3c5dc36836e0-Paper-Conference.pdf), [Salience DETR](https://openaccess.thecvf.com/content/CVPR2024/papers/Hou_Salience_DETR_Enhancing_Detection_Transformer_with_Hierarchical_Salience_Filtering_Refinement_CVPR_2024_paper.pdf), [RT-DERT](https://openaccess.thecvf.com/content/CVPR2024/papers/Zhao_DETRs_Beat_YOLOs_on_Real-time_Object_Detection_CVPR_2024_paper.pdf), [RDMNet](https://ieeexplore.ieee.org/abstract/document/10636782/), and [RodNet](https://ieeexplore.ieee.org/abstract/document/10144555)

- **Restoration methods (used pre-trained models)**: [MIRNet-v2](https://github.com/swz30/MIRNetv2), [CSEC](https://github.com/yiyulics/CSEC), [ConvIR](https://github.com/c-yn/ConvIR), [UDR-S2Former](https://github.com/Ephemeral182/UDR-S2Former_deraining), and [Restormer](https://github.com/swz30/Restormer).
---

## Acknowledgement

The codebase is built upon [Ultralytics](https://github.com/ultralytics/ultralytics) and [YOLOv10](https://github.com/THU-MIG/yolov10).  
We sincerely thank the authors of the RNT and RID datasets for making their benchmarks publicly available, and the broader object detection community for their foundational contributions.
