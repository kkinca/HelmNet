# HelmNet

A computer vision project for detecting worker helmet compliance using deep learning and transfer learning.

## Project Overview

In hazardous environments such as construction sites and industrial facilities, ensuring that workers wear safety helmets is critical. Manual monitoring is labor-intensive, difficult to scale, and prone to inconsistency.

This project builds an image classification system that detects whether a worker is wearing a safety helmet. The goal is to support automated workplace safety monitoring that can eventually be integrated with camera systems for near-real-time compliance detection.  [oai_citation:0‡Computer Vision-Project Presentation Template FINAL.pdf](sediment://file_000000005a2071fd9ebe3828178b72f8)

## Business Problem

Head injuries are among the most severe and preventable workplace risks. Safety teams need faster, more scalable ways to monitor helmet usage across job sites.

This project explores how computer vision can help:
- improve safety compliance
- reduce dependence on manual inspections
- support faster response to violations
- enable scalable monitoring across multiple locations  [oai_citation:1‡Computer Vision-Project Presentation Template FINAL.pdf](sediment://file_000000005a2071fd9ebe3828178b72f8)  [oai_citation:2‡Computer Vision-Project Presentation Template FINAL.pdf](sediment://file_000000005a2071fd9ebe3828178b72f8)

## Dataset

The working dataset contains **631 labeled images** of workers in industrial environments:
- **With Helmet:** 311 images
- **Without Helmet:** 320 images

Key characteristics:
- balanced class distribution
- RGB images
- image size standardized for modeling
- variation in lighting, camera angles, background clutter, and worker positioning  [oai_citation:3‡Computer Vision-Project Presentation Template FINAL.pdf](sediment://file_000000005a2071fd9ebe3828178b72f8)  [oai_citation:4‡Computer Vision-Project Presentation Template FINAL.pdf](sediment://file_000000005a2071fd9ebe3828178b72f8)

## Data Preprocessing

The dataset was prepared for deep learning with the following steps:
- resized images for model compatibility
- split data into training, validation, and test sets
  - Training: 70%
  - Validation: 15%
  - Test: 15%
- normalized pixel values from 0-255 to 0-1
- retained RGB format to support VGG16 input requirements  [oai_citation:5‡Computer Vision-Project Presentation Template FINAL.pdf](sediment://file_000000005a2071fd9ebe3828178b72f8)

## Modeling Approach

Four deep learning models were developed and compared:

1. **Simple CNN**
   - baseline convolutional neural network built from scratch

2. **VGG16 Transfer Learning**
   - pretrained VGG16 used as a feature extractor

3. **VGG16 + FFNN**
   - VGG16 with additional dense layers for classification

4. **VGG16 + FFNN + Data Augmentation**
   - augmentation added to improve robustness and reduce overfitting on a small dataset  [oai_citation:6‡Computer Vision-Project Presentation Template FINAL.pdf](sediment://file_000000005a2071fd9ebe3828178b72f8)

## Model Performance

| Model | Validation Accuracy | Notes |
|---|---:|---|
| Simple CNN | 98.9% | Strong baseline |
| VGG16 (Base) | 100% | Major improvement from transfer learning |
| VGG16 + FFNN | 98.9% | Added complexity without improvement |
| VGG16 + FFNN + Data Augmentation | 100% | Best practical choice | 

The final model selected was **VGG16 + FFNN + Data Augmentation** because it matched the highest validation accuracy while offering stronger practical robustness for real-world image variation.  [oai_citation:7‡Computer Vision-Project Presentation Template FINAL.pdf](sediment://file_000000005a2071fd9ebe3828178b72f8)  [oai_citation:8‡Computer Vision-Project Presentation Template FINAL.pdf](sediment://file_000000005a2071fd9ebe3828178b72f8)

## Final Model Selection

The final model achieved:
- **100% validation accuracy**
- **100% test accuracy**

It was selected because data augmentation helps the model generalize better to differences in lighting, orientation, scale, and worker pose, which is especially important when working with a relatively small dataset.  [oai_citation:9‡Computer Vision-Project Presentation Template FINAL.pdf](sediment://file_000000005a2071fd9ebe3828178b72f8)

## Business Impact

This project demonstrates how computer vision can shift workplace safety monitoring from a manual, reactive process to an automated, proactive one.

Potential business benefits include:
- enhanced safety compliance
- reduced labor costs from manual inspections
- faster identification of violations
- more standardized enforcement
- scalability across job sites using existing camera infrastructure  [oai_citation:10‡Computer Vision-Project Presentation Template FINAL.pdf](sediment://file_000000005a2071fd9ebe3828178b72f8)

## Recommendations

Recommended next steps for deployment:
- integrate the model with camera systems
- implement real-time alerts for violations
- retrain periodically with new site images
- expand detection to other safety equipment such as vests, gloves, and goggles
- pilot at a single site before scaling more broadly  [oai_citation:11‡Computer Vision-Project Presentation Template FINAL.pdf](sediment://file_000000005a2071fd9ebe3828178b72f8)

## Tools and Techniques

- Python
- Computer Vision
- Deep Learning
- Convolutional Neural Networks (CNN)
- Transfer Learning
- VGG16
- Data Augmentation
- Image Classification

## Key Takeaway

Transfer learning significantly outperformed the baseline CNN, and the augmented VGG16-based model emerged as the strongest deployment-ready solution for helmet compliance detection on this dataset.  [oai_citation:12‡Computer Vision-Project Presentation Template FINAL.pdf](sediment://file_000000005a2071fd9ebe3828178b72f8)

One note: GitHub README files should not include citation markup, so here’s the same version cleaned for direct GitHub paste:

# HelmNet

A computer vision project for detecting worker helmet compliance using deep learning and transfer learning.

## Project Overview

In hazardous environments such as construction sites and industrial facilities, ensuring that workers wear safety helmets is critical. Manual monitoring is labor-intensive, difficult to scale, and prone to inconsistency.

This project builds an image classification system that detects whether a worker is wearing a safety helmet. The goal is to support automated workplace safety monitoring that can eventually be integrated with camera systems for near-real-time compliance detection.

## Business Problem

Head injuries are among the most severe and preventable workplace risks. Safety teams need faster, more scalable ways to monitor helmet usage across job sites.

This project explores how computer vision can help:
- improve safety compliance
- reduce dependence on manual inspections
- support faster response to violations
- enable scalable monitoring across multiple locations

## Dataset

The working dataset contains **631 labeled images** of workers in industrial environments:
- **With Helmet:** 311 images
- **Without Helmet:** 320 images

Key characteristics:
- balanced class distribution
- RGB images
- image size standardized for modeling
- variation in lighting, camera angles, background clutter, and worker positioning

## Data Preprocessing

The dataset was prepared for deep learning with the following steps:
- resized images for model compatibility
- split data into training, validation, and test sets
  - Training: 70%
  - Validation: 15%
  - Test: 15%
- normalized pixel values from 0-255 to 0-1
- retained RGB format to support VGG16 input requirements

## Modeling Approach

Four deep learning models were developed and compared:

1. **Simple CNN**
   - baseline convolutional neural network built from scratch

2. **VGG16 Transfer Learning**
   - pretrained VGG16 used as a feature extractor

3. **VGG16 + FFNN**
   - VGG16 with additional dense layers for classification

4. **VGG16 + FFNN + Data Augmentation**
   - augmentation added to improve robustness and reduce overfitting on a small dataset

## Model Performance

| Model | Validation Accuracy | Notes |
|---|---:|---|
| Simple CNN | 98.9% | Strong baseline |
| VGG16 (Base) | 100% | Major improvement from transfer learning |
| VGG16 + FFNN | 98.9% | Added complexity without improvement |
| VGG16 + FFNN + Data Augmentation | 100% | Best practical choice |

The final model selected was **VGG16 + FFNN + Data Augmentation** because it matched the highest validation accuracy while offering stronger practical robustness for real-world image variation.

## Final Model Selection

The final model achieved:
- **100% validation accuracy**
- **100% test accuracy**

It was selected because data augmentation helps the model generalize better to differences in lighting, orientation, scale, and worker pose, which is especially important when working with a relatively small dataset.

## Business Impact

This project demonstrates how computer vision can shift workplace safety monitoring from a manual, reactive process to an automated, proactive one.

Potential business benefits include:
- enhanced safety compliance
- reduced labor costs from manual inspections
- faster identification of violations
- more standardized enforcement
- scalability across job sites using existing camera infrastructure

## Recommendations

Recommended next steps for deployment:
- integrate the model with camera systems
- implement real-time alerts for violations
- retrain periodically with new site images
- expand detection to other safety equipment such as vests, gloves, and goggles
- pilot at a single site before scaling more broadly

## Tools and Techniques

- Python
- Computer Vision
- Deep Learning
- Convolutional Neural Networks (CNN)
- Transfer Learning
- VGG16
- Data Augmentation
- Image Classification

## Key Takeaway

Transfer learning significantly outperformed the baseline CNN, and the augmented VGG16-based model emerged as the strongest deployment-ready solution for helmet compliance detection on this dataset.

I’d use the second version in GitHub.
