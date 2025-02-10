# Object Detection System

## Overview
This project utilizes a pre-trained YOLOv8 model to detect objects in images and videos. The system is implemented using Python and the Ultralytics YOLO library. The Jupyter Notebook provides step-by-step instructions for setting up and running the object detection pipeline.

## Features
- Uses a pre-trained YOLOv8 model for object detection.
- Processes images and videos.
- Saves processed outputs to a specified directory.

## Installation
Before running the notebook, ensure that the required dependencies are installed.

```sh
pip install ultralytics
```

## Usage

### 1. Mount Google Drive
The notebook is designed to run on Google Colab and uses Google Drive to store models and output files. Before running the model, mount Google Drive:

```python
from google.colab import drive
drive.mount('/content/drive')
```

### 2. Load YOLOv8 Model
Load the pre-trained YOLOv8 model from the specified path:

```python
from ultralytics import YOLO
model = YOLO('/content/drive/MyDrive/Code-Clause-Projects/yolov8m.pt')
```

### 3. Perform Object Detection on Images
Specify the input image path and process it using the YOLO model:

```python
image_path = "/content/drive/MyDrive/Code-Clause-Projects/testing-images-yolo/image-04.png"
results = model.predict(source=image_path, save=True, project=output_folder, name="yolo_output")
```

### 4. Save and View Results
The processed output will be saved in the designated folder:

```sh
Processed image saved in: /content/drive/MyDrive/Code-Clause-Projects/output-images/yolo_output/
```

## Folder Structure
```
Object_Detection_System/
├── Object_Detection_System.ipynb  # Jupyter Notebook for object detection
├── yolov8m.pt                      # Pre-trained YOLOv8 model
├── testing-images-yolo/            # Input images for object detection
├── output-images/                  # Processed images and videos
```

## Sample Data and Model
To access sample input videos, images, and the pre-trained model, visit the following link:

[Sample Data and Model](https://drive.google.com/drive/folders/1HfJoy32nfDnDriVh2kIIVRodPTioxaU-?usp=sharing)

## Requirements
- Python 3.8+
- Google Colab (recommended)
- Ultralytics YOLO
- Google Drive (for storage)

## License
This project is for educational and research purposes. Ensure proper usage of the YOLO model as per its licensing terms.

## Acknowledgments
- Ultralytics for providing YOLO models
- Google Colab for cloud-based execution

