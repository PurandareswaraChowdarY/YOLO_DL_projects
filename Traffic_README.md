# 🚦 Traffic Object Detection with YOLOv8

This project demonstrates how to train a custom YOLOv8 model to detect traffic-related objects: **Person, Car, Traffic Light, and Stop Sign** using the Ultralytics `yolov8` library.

---

## 📁 Dataset Structure  
Make sure your dataset is arranged in the following structure:

<pre>
traffic_dataset/
├── images/
│   ├── train/
│   ├── val/
│   └── test/              
├── labels/
│   ├── train/
│   ├── val/
│   └── test/              
└── traffic_config.yaml
</pre>

Each image must have a corresponding `.txt` file in the `labels/` folder, formatted in **YOLO format**:  
`<class_id> <x_center> <y_center> <width> <height>` — all values must be **normalized (0 to 1)**.

---

Installation of required libraries:

pip install ultralytics opencv-python
