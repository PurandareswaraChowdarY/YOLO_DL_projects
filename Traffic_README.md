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

## ⚙️ traffic_config.yaml

```yaml
path: C:/Users/pandu/Pictures/traffic_dataset  # update this to your dataset's root path
train: images/train
val: images/val
test: images/test  # optional
names:
  0: Person
  1: Car
  2: Traffic Light
  3: Stop Sign
