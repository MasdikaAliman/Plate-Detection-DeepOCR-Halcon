# Alat Pendeteksi Lalu Lintas Berbasis Deep Learning

This project leverages deep learning techniques for license plate detection and DeepOCR using HALCON 23.11-Progress Software.

## Requirements

- [HALCON 23.11](https://www.mvtec.com/downloads/halcon)
- A labeled dataset of license plates

## Step-by-Step Guide

### 1. Prepare Your Dataset

Modify the dataset path in `prepare_data_detection.hdev`:


* Set the path to your dataset directory
```
ExampleDataDir := '/home/dika/Documents/PKM_program/Dataset/Plate'
```
Run `prepare_data_detection.hdev` to prepare the dataset for training.

### 2. Train Your Model

Modify the data directory path in `train_data_detection.hdev` to point to the prepared dataset:

* Update with your dataset path
```
dataDir := 'path_from_ur_prepare_dataset'
```
Run `train_data_detection.hdev` to start training your model.

### 3. Running Plate Detection and OCR

After training, update the model paths in `PlateDetectionDeepOCR.hdev` with the appropriate file locations:

* Set the paths for the preprocess parameters and trained model
```
PreprocessParamFileName := '/home/dika/Documents/PKM_program/Deteksink/detect_plat_data/dldataset_plat512x320dl_preprocess_param.hdict'
TrainedModelFileName := '/home/dika/Documents/PKM_program/Deteksink/detect_plat_data/best_dl_model_detection.hdl'
```
Once the paths are updated, you can run the plate detection and OCR using this script.

## Results Detection
