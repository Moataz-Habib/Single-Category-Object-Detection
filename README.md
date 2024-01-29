# Single-Category Object Detection 

## Table of Contents
- [Introduction](#introduction)
- [Data Processing](#data-processing)
- [Model Training and Testing](#model-training-and-testing)
- [Model Configurations](#model-configurations)
- [Ablation Study Results](#ablation-study-results)
- [Prediction Results](#prediction-results)
- [Conclusion](#conclusion)

## Introduction

This project aims to enhance Single-Category Object Detection by experimenting with various configurations of the YOLO V8 model. We focus on optimizing model performance, particularly on one category, to assess the trade-offs between accuracy and computational efficiency.

## Data Processing: 

The data consists of video frames, with preprocessing involving normalization, resizing, and applying Gaussian blur. The data setup is organized into folders, each containing 30 videos of 2 seconds duration at 12 frames per second resulting in a total of 720 frames per folder.

## Model Training and Testing

The data is divided into 60% training, 20% validation, and 20% testing sets. The directory structure is as follows:

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
Our ablation study spans across multiple YOLO V8 configurations to pinpoint the optimal model structure:

- Baseline YOLO V8 Nano
- Enhanced YOLO V8 Nano with added layers
- YOLO V8 Nano with batch normalization and increased repeats
- YOLO V8 Nano with a modified detect layer
- Comparative analysis using YOLO V8 S

## Ablation Study Results

Each configuration's performance was evaluated using Precision-Recall curves. The visual comparison underscores the impact of each modification on the model's precision.

<table>
<tr>
<th>Configuration</th>
<th>Precision-Recall Curve</th>
</tr>
<tr>
<td>Baseline YOLO V8 Nano</td>
<td><img src="images/img1.png" alt="Baseline YOLO V8 Nano" width="300" /></td>
</tr>
<tr>
<td>Adding Layers</td>
<td><img src="images/img2.png" alt="Adding Layers" width="300" /></td>
</tr>
<tr>
<td>Batch Normalization</td>
<td><img src="images/img3.png" alt="Batch Normalization" width="300" /></td>
</tr>
<tr>
<td>Modified Detect Layer</td>
<td><img src="images/img4.png" alt="Modified Detect Layer" width="300" /></td>
</tr>
<tr>
<td>YOLO V8 S</td>
<td><img src="images/img5.png" alt="YOLO V8 S" width="300" /></td>
</tr>
</table>

For a visual representation of the prediction capabilities and the comparative performance across different model configurations, please see the [`runs` folder](https://github.com/Moataz-Habib/Single-Category-Object-Detection/tree/main/runs) and the detailed prediction results showcased in the repository.


## Prediction Results
To assess the practical applicability of the models, their prediction results were evaluated. The following are the outcomes showcasing the detection capabilities of each configuration:

<table>
<tr>
<th>Configuration</th>
<th>Prediction Result</th>
</tr>
<tr>
<td>Baseline YOLO V8 Nano</td>
<td><img src="images/img6.jpg" alt="Prediction Result for Baseline YOLO V8 Nano" width="300" /></td>
</tr>
<tr>
<td>Adding Layers</td>
<td><img src="images/img7.jpg" alt="Prediction Result for Adding Layers" width="300" /></td>
</tr>
<tr>
<td>Batch Normalization</td>
<td><img src="images/img8.jpg" alt="Prediction Result for Batch Normalization" width="300" /></td>
</tr>
<tr>
<td>Modified Detect Layer</td>
<td><img src="images/img9.jpg" alt="Prediction Result for Modified Detect Layer" width="300" /></td>
</tr>
<tr>
<td>YOLO V8 S</td>
<td><img src="images/img10.jpg" alt="Prediction Result for YOLO V8 S" width="300" /></td>
</tr>
</table>


## Conclusion

The ablation study conducted on various configurations of the YOLO V8 model demonstrated that strategic modifications could significantly enhance object detection performance. While the baseline YOLO V8 Nano and the variations with added layers and batch normalization maintained high precision-recall scores, the YOLO V8 S configuration stood out with the highest mAP of 0.977 and exhibited superior detection precision in practical scenarios.

These findings suggest that the YOLO V8 S model, with its advanced architecture, offers a substantial improvement in detection accuracy, making it an excellent candidate for real-world applications where precision is paramount. The prediction results, particularly for the YOLO V8 S model, confirm its robustness and reliability in detecting objects with high confidence.

For a deeper dive into the methodology and the code that powered these experiments, the [Single Category Object Detection notebook](https://github.com/Moataz-Habib/Single-Category-Object-Detection/blob/main/Single%20Category%20Object%20Detection.ipynb) is available for review. The comprehensive analysis contained within illustrates the potential of YOLO V8 modifications to push the boundaries of object detection technology, especially in single-category detection tasks.

The project's success encourages future explorations to further optimize these models for speed and accuracy, potentially extending their application to more complex multi-category detection scenarios and deployment on edge devices with resource constraints.

For a visual representation of the prediction capabilities and the comparative performance across different model configurations, please see the [`runs` folder](https://github.com/Moataz-Habib/Single-Category-Object-Detection/tree/main/runs) and the detailed prediction results showcased in the repository.


