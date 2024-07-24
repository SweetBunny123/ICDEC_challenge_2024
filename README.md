# ICDEC 2024 Vehicle Detection Challenge

![ICDEC 2024 Logo]([path_to_logo_image.png](https://d8it4huxumps7.cloudfront.net/uploads/images/150x150/uploadedManual-666743b42746f_screenshot_2024-06-07_014453.png?d=200x200))

## 🚗 Challenge Overview

Welcome to our submission for the ICDEC 2024 Vehicle Detection in Various Weather Conditions (VDVWC) Challenge! This repository contains our innovative approach to detecting vehicles across diverse weather and lighting conditions.

### 🎯 Objective

To develop a robust vehicle detection model that performs accurately across various weather conditions, improving upon existing methods that primarily focus on natural weather scenarios.

## 📊 Dataset

We utilized the AVD-Dataset, comprising 3,200 images of vehicles in various weather conditions:

- 2,600 images for training
- 200 images for validation
- Annotations provided in YOLO format

**Dataset Link**: [AVD-Dataset](https://github.com/Sourajit-Maity/juvdv2-vdvwc.git)

## 🛠 Methodology

Our approach leverages state-of-the-art deep learning techniques, specifically:

1. **YOLOv8**: We employed the latest YOLOv8 architecture, known for its speed and accuracy in object detection tasks.
2. **Custom Augmentations**: Implemented extensive data augmentation to simulate various weather conditions.
3. **Transfer Learning**: Utilized pre-trained weights and fine-tuned on the AVD-Dataset.
4. **Hyperparameter Optimization**: Conducted thorough hyperparameter tuning to maximize model performance.

(Add more details about your specific methodology here)

## 📈 Results

Our model achieved the following performance metrics on the validation set:

- mAP: X.XX
- F1-Score: X.XX

(Include any visualizations or additional performance metrics here)

## 🛠 Methodology

Our approach leverages state-of-the-art deep learning techniques, specifically YOLOv8, with a multi-stage training strategy:

1. **YOLOv8 Architecture**: We employed the latest YOLOv8 model, known for its speed and accuracy in object detection tasks.

2. **Multi-Stage Training**:
   a. **Stage 1 - Sunny Conditions** (20 epochs):
      - Initial training using only images captured in sunny conditions.
      - This stage helps the model learn basic features and object representations in ideal lighting conditions.
   
   b. **Stage 2 - Full Dataset** (20 epochs):
      - Fine-tuning on the entire dataset, including all weather conditions.
      - This stage exposes the model to diverse weather scenarios, improving its generalization capabilities.
   
   c. **Stage 3 - Final Refinement** (5 epochs):
      - A short fine-tuning phase on the full dataset.
      - This stage helps in final adjustments and stabilization of the model's performance across all conditions.

3. **Custom Augmentations**: Implemented extensive data augmentation to simulate various weather conditions and enhance model robustness.

4. **Transfer Learning**: Utilized pre-trained weights as a starting point, then fine-tuned through our multi-stage process.

5. **Hyperparameter Optimization**: Conducted thorough hyperparameter tuning at each stage to maximize model performance.

This staged approach allows the model to first grasp fundamental vehicle detection in optimal conditions, then gradually adapt to more challenging scenarios, potentially leading to improved overall performance and generalization.

(Add any additional details specific to your implementation here)
