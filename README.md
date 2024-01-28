# Single-Category Object Detection 

## Table of Contents
1. [Introduction](#introduction)
2. [Dataset Structure](#dataset-structure)
3. [Model Configurations](#model-configurations)
4. [Ablation Study Results](#ablation-study-results)
5. [Precision Results](#precision-results)
6. [Conclusion](#conclusion)
7. [Acknowledgements](#acknowledgements)

## Introduction
This repository hosts our Single-Category Object Detection project, which explores various configurations of the YOLO V8 model, including Nano and S versions, to optimize detection performance for a single category.

## Dataset Structure
The dataset is partitioned into training, validation, and test subsets with the following directory layout:

dataset/
├── train/
│ ├── images/
│ └── labels/
├── val/
│ ├── images/
│ └── labels/
└── test/
├── images/
└── labels/


## Model Configurations
The project evaluates multiple YOLO V8 architectures:
- Baseline YOLO V8 Nano
- YOLO V8 Nano with additional layers
- YOLO V8 Nano with batch normalization and more repeats
- YOLO V8 Nano with an altered detect layer
- YOLO V8 S for comparative purposes

## Ablation Study Results
The following table shows the Precision-Recall curves obtained from each model configuration:

| Configuration | Precision-Recall Curve |
|---------------|------------------------|
| Baseline YOLO V8 Nano | ![Baseline YOLO V8 Nano](imagesimg1.png) |
| Adding Layers | ![Adding Layers](images/img2.png) |
| Batch Normalization | ![Batch Normalization](images/img3.png) |
| Modified Detect Layer | ![Modified Detect Layer](images/img4.png) |
| YOLO V8 S | ![YOLO V8 S](images/img5.png) |

## Precision Results
This section showcases the precision of object detection across all the models we tested:

| Configuration | Precision Image |
|---------------|-----------------|
| Baseline YOLO V8 Nano | ![Precision Baseline](images/Precision_baseline.png) |
| Adding Layers | ![Precision Adding Layers](images/Precision_adding_layers.png) |
| Batch Normalization | ![Precision Batch Normalization](images/Precision_batch_norm.png) |
| Modified Detect Layer | ![Precision Modified Detect Layer](images/Precision_detect_layer.png) |
| YOLO V8 S | ![Precision YOLO V8 S](images/Precision_yolov8s.png) |

## Conclusion
Modifications to the detect layer in the YOLO V8 Nano architecture demonstrated significant improvements in detection precision. Detailed analysis and code can be found in the [Single Category.ipynb](https://github.com/FrozenWanderer/Single-Category-Object-Detection/blob/main/Single%20Category.ipynb) notebook.

## Acknowledgements
We extend our heartfelt gratitude to all individuals who contributed to this research and helped facilitate the project's success.

---

**Note:** Ensure you upload the Precision-Recall curve and precision images to the specified `images/` directory in your GitHub repository and update the image paths in the tables accordingly. The provided mAP scores and file paths are placeholders and should be updated with your actual data.



