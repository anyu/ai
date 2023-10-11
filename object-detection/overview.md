# Overview

Combines image classification and object localization.

## Two-stage object detection algorithms
- multiple iterations of the same image
- uses selective regions to apply classifiers (good, but slow)
- high accuracy, but slower

The two-stage architecture first find a region of interest and uses this cropped region for classification:
1. Object region proposal with conventional CV methods or deep networks
2. Object classification based on features extracted from the proposed region with bounding-box regression.

### RCNN (Regions w/ CNN)
- Fast-RCNN, Faster-RCNN models were faster but still not real-time
- Mask R-CNN
- G-RCNN

## One-stage object detection algorithms
- predicts bounding boxes over the images without the region proposal step.
- runs object detection in real-time
- more efficient, as it uses a single pass to make a prediction of the objects

### YOLO (You Only Look Once) and its subsequent versions
- may be most common model nowadays

### SSD (Single Shot MultiBox Detector)


## Metrics for evaluating object detection models
1. How good is the location
1. How good is the classificaton

IoU (intersection over union) - how close the predicted bounding box is to the ground truth; a value between 0 and 1
- IoU = 1, exactly as predicted
- IoU = 0, no overlap

Calculated = area of intersection / area of union

Confusion matrix
- matrix of predicted vs. truth


- There are many object detection metrics, but people mostly use mean Average Precision (mAP) and the make plots if they want details about failures.
- Conv-nets are out, vision transformers (focal nets!) are in.
- Pre-training on image-net is more computationally expensive than - pre-training using self-supervised learning.
- Transfer learning applied to object detection in videos is an under-studied niche!