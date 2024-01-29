# Single-Category Object Detection 

## Table of Contents
1. [Introduction](#introduction)
2. [Dataset Structure](#dataset-structure)
3. [Model Configurations](#model-configurations)
4. [Ablation Study Results](#ablation-study-results)
5. [Precision Results](#precision-results)
6. [Conclusion](#conclusion)


## Introduction
This repository hosts our Single-Category Object Detection project, which explores various configurations of the YOLO V8 model, including Nano and S versions, to optimize detection performance for a single category.

## Data Processing: 

The data consists of video frames, with preprocessing involving normalization, resizing, and applying Gaussian blur. The data setup is organized into folders, each containing 30 videos of 2 seconds duration at 12 frames per second resulting in a total of 720 frames per folder.

## Model Training and Testing

The data is divided into 60% training, 20% validation, and 20% testing sets. The dataset is structured as follows:

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

Training Process: Adjustments are made to the image and label formats to comply with YOLO requirements, followed by training over 100 epochs.

## Model Configurations
The project evaluates multiple YOLO V8 architectures:
- Baseline YOLO V8 Nano
- YOLO V8 Nano with additional layers
- YOLO V8 Nano with batch normalization and more repeats
- YOLO V8 Nano with an altered detect layer
- YOLO V8 S for comparative purposes

## Ablation Study Results
The following table shows the Precision-Recall curves obtained from each model configuration:

<table>
<tr>
<th>Configuration</th>
<th>Baseline YOLO V8 Nano</th>
<th>Adding Layers</th>
<th>Batch Normalization</th>
<th>Modified Detect Layer</th>
<th>YOLO V8 S</th>
</tr>
<tr>
<td>Precision-Recall Curve</td>
<td><img src="images/img1.png" alt="Baseline YOLO V8 Nano" width="1500" /></td>
<td><img src="images/img2.png" alt="Adding Layers" width="1500" /></td>
<td><img src="images/img3.png" alt="Batch Normalization" width="1500" /></td>
<td><img src="images/img4.png" alt="Modified Detect Layer" width="1500" /></td>
<td><img src="images/img5.png" alt="YOLO V8 S" width="1500" /></td>
</tr>
</table>



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

