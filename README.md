<div align="center">

DiffKA
---

### DiffKA: Diffusion-based Knowledge Absorption Approach for Robust Object Detection in Challenging Weather Conditions

<p align="center">
  <img src="DiffKA.png" width="90%"><br>
  <b>DiffKA Architecture</b>
</p>

</div>

---

## Introduction

DDiffKA is a novel approach for robust object detection under rainy nighttime weather conditions. The model leverages a diffusion-based knowledge absorption mechanism that enables the detector to effectively learn clean features from degraded images. Comprehensive evaluations on various datasets demonstrate that DiffKA acquires the highest performance, outperforming existing methods on two benchmark datasets, including a rainy nighttime (RNT) dataset and a Rain in Driving (RID) dataset.

---

## Datasets

### RNT Dataset — Rainy Night Dataset

- **Paper:** [Multilevel knowledge transmission for object detection in rainy night weather conditions](https://ieeexplore.ieee.org/abstract/document/10541873)
- A challenging benchmark containing real-world images captured under rainy nighttime conditions, designed to evaluate object detection robustness in combined rain and low-light degradation.

### RID Dataset — Rain In Driving

- **Paper:** [Single Image Deraining: A Comprehensive Benchmark Analysis (CVPR 2019)](https://openaccess.thecvf.com/content_CVPR_2019/html/Li_Single_Image_Deraining_A_Comprehensive_Benchmark_Analysis_CVPR_2019_paper.html)
- A comprehensive deraining benchmark collected from driving scenarios, providing paired rainy/clean image sets for training and evaluating detection models under rain degradation.

---

## Trained Weights

Pre-trained model weights for DiffKA are available below:

| Model | Dataset | Download |
|-------|---------|----------|
| DiffKA_model | RNT + RID | [Download](https://github.com/val-utehy/DiffKA/raw/refs/heads/main/DiffKA_model.pt) |

Place the downloaded weights at the root of the repository:

```
DiffKA_model.pt
```

---

## Inference

```python
from ultralytics import YOLO

weights_path = "DiffKA_model.pt"

model = YOLO(weights_path)

results = model.predict(
    source="path/to/image_or_folder",
    imgsz=640,
    conf=0.25,
    iou=0.6,
    save=True
)

print("Inference completed.")
```

---

## Acknowledgement

The codebase is built upon [Ultralytics](https://github.com/ultralytics/ultralytics) and [YOLOv10](https://github.com/THU-MIG/yolov10).  
We sincerely thank the authors of the RNT and RID datasets for making their benchmarks publicly available, and the broader object detection community for their foundational contributions.