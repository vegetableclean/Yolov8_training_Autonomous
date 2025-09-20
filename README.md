# YOLOv8 Training with Qcars

This repository contains code and resources for training **YOLOv8** (You Only Look Once version 8) on **Qcars** datasets. The aim of this project is to demonstrate how to leverage YOLOv8 for object detection tasks, specifically tailored for identifying objects in Qcars2 datasets.

## Overview

**YOLOv8** is the latest version of the YOLO family of object detection models. This repository focuses on using YOLOv8 to train on datasets related to **Qcars**. By utilizing the power of YOLOv8, the model can be trained to detect various objects with high accuracy and speed.

## Key Features

- **YOLOv8 Implementation:** All necessary code and configurations to train YOLOv8 on the Qcars dataset.
- **Qcars Dataset Integration:** Instructions on how to download and prepare the Qcars dataset for YOLOv8 training.
- **Custom Training Pipeline:** End-to-end pipeline for training, evaluating, and testing the YOLOv8 model on your specific Qcars data.
- **Pre-trained Models:** Pre-trained weights for faster transfer learning or to start from a baseline.
- **Evaluation Metrics:** Tools for evaluating model performance using standard object detection metrics.

## Requirements

Before you start, ensure you have the following installed:

- **Python 3.7+**
- **PyTorch 1.9+**
- **CUDA (Optional)**: For GPU acceleration
- **Dependencies:** You can install all required dependencies via the following:

```bash
pip install -r requirements.txt


## Guidelines
Some suggestions for training your own dataset. Here are some guidelines:

Manually label detection dataset (bounding boxes) and train a rough yolo detection network. The bounding box doesn’t need to be very accurate as long as it’s larger than the objects.
Use the same training configuration file as COCO dataset.
The class ID for QCar was 2, same as “car” in COCO dataset.
Download pretrained YOLO detection model from Ultralytics and train extra epochs with customized dataset containing QCar data.
Use segment anything model (SAM) and custom YOLO detection model to create segmentation dataset and train the YOLO segmentation model
After collecting enough images data containing objects of interest (QCar, road signs, traffic lights etc.), use YOLO detection model to classify and estimate bounding boxes.
Use SAM on each bounding box to get the segmentation mask of the object.
pair the class IDs from the detection model and the segmentation masks from SAM to create the label for that image.
Manually go through the preliminary segmentation dataset to remove any poorly labeled data
Download a pretrained YOLO segmentation model from Ultralytics and train extra epochs with the new dataset.
