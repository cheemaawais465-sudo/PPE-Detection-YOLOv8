# Personal Protective Equipment (PPE) Detection using YOLOv8

## Project Overview

This project focuses on developing a Computer Vision based Personal Protective Equipment (PPE) Detection System using YOLOv8n.

The system detects PPE-related objects in images and identifies whether workers are wearing required safety equipment such as hardhats and safety vests.

## Objective

The main objective of this project is to develop an object detection system that can assist in workplace safety monitoring by detecting PPE compliance.

The model detects five classes:

* Person
* Hardhat
* Safety Vest
* NO-Hardhat
* NO-Safety Vest

## Applications

* Construction site safety monitoring
* Factory safety monitoring
* Industrial workplace safety
* PPE compliance monitoring
* Automated safety inspection

## Dataset

The project uses a PPE detection dataset containing 1,387 images.

| Split      | Images |
| ---------- | -----: |
| Training   |    967 |
| Validation |    284 |
| Testing    |    136 |
| Total      |  1,387 |

At least 100 images were manually annotated using Roboflow as required by the project assignment.

## Class Mapping

| Class ID | Class Name     |
| -------: | -------------- |
|        0 | Person         |
|        1 | Hardhat        |
|        2 | Safety Vest    |
|        3 | NO-Hardhat     |
|        4 | NO-Safety Vest |

## Tools and Technologies

* Python
* Google Colab
* YOLOv8n
* Ultralytics
* Roboflow
* PyTorch
* OpenCV
* Matplotlib
* Pandas
* Google Drive

## Model Training

The YOLOv8n pretrained model was trained for 30 epochs using 640 × 640 image size on an NVIDIA Tesla T4 GPU.

The trained model is saved as `best.pt`.

## Model Evaluation

| Metric       | Result |
| ------------ | -----: |
| Precision    | 81.55% |
| Recall       | 57.07% |
| mAP@0.5      | 64.25% |
| mAP@0.5:0.95 | 38.70% |

The evaluation includes training and validation curves, Precision-Recall curve, F1 curve, confusion matrix and per-class analysis.

## Inference

The trained model was tested on unseen test images. The predictions include bounding boxes, class names and confidence scores.

At least 15 prediction images were generated as required by the assignment.

## Error Analysis

Ten prediction images were manually reviewed to identify incorrect or weak predictions.

Common issues included over-detection, false positives, missed objects and wrong class predictions.

Possible improvements include collecting more diverse training data, improving annotation consistency, using challenging images, applying suitable data augmentation and experimenting with larger YOLO models.

## Project Structure

```text
PPE-Detection-YOLOv8/
├── README.md
├── data.yaml
├── best.pt
├── predictions/
├── training_results/
├── final_report.pdf
└── PPE_Detection_YOLOv8.ipynb
```

## Future Improvements

1. Collect more diverse PPE images.
2. Improve annotation quality and consistency.
3. Train for more epochs.
4. Apply additional data augmentation.
5. Experiment with larger YOLO models.
6. Improve detection of small and partially visible PPE objects.
7. Implement real-time video detection.

## Project Resources

**Google Drive:** Add your Google Drive project link here.

**Google Colab Notebook:** Add your Google Colab notebook link here.

**Final Report:** Included in the project resources.

## Conclusion

This project demonstrates the development of a YOLOv8n-based PPE detection system for workplace safety monitoring. The model detects five PPE-related classes and provides bounding boxes, class labels and confidence scores.

