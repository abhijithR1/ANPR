# **Automatic Number Plate Recognition (ANPR) with YOLOv9 and EasyOCR**

## **Description**

This project implements an Automatic Number Plate Recognition (ANPR) system using the YOLOv9 object detection model and EasyOCR for text recognition. The system is capable of detecting vehicle license plates in images or videos and extracting the text from the plates.

The project leverages a custom-trained YOLOv9 model for accurate license plate detection, followed by EasyOCR to recognize the text from the detected plates. The model is trained on a dataset sourced from [Roboflow](https://universe.roboflow.com/arvind-kumar-wjygd/anpr2-syxl7) and can be further fine-tuned or validated with new data.

### **Key Steps:**
- Setting up the environment for GPU-based training and inference.
- Downloading and using pre-trained YOLOv9 weights for license plate detection.
- Training a custom YOLOv9 model on a specialized ANPR dataset.
- Validating and performing inference with the trained model.

### **YOLOv9 for Detection and EasyOCR for Text Recognition:**

During the training phase, we used the `detect.py` file to detect vehicle license plates. The `detect.py` script successfully identifies the bounding boxes around the plates in images or videos. However, to annotate the license plate number on top of the detected region, we use the `ANPR.py` file.

### **Important Note:**
Before combining YOLOv9 and EasyOCR, make sure to upload the `anpr.py` file to your folder to avoid any errors related to missing files during execution.

The `ANPR.py` script integrates EasyOCR into the process, enabling the system to detect and recognize the characters on the license plate. This file handles the OCR part of the system, which extracts the text from the detected plates and annotates it above the bounding boxes.

### **Use Cases:**
This project is beneficial for use cases such as:
- Traffic monitoring and management.
- Automated vehicle entry systems.
- Automated toll collection systems.
