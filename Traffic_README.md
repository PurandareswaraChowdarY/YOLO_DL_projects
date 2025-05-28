# 🚦 Traffic Object Detection with YOLOv8

This project implements object detection on traffic-related objects using the YOLOv8 model by Ultralytics. The dataset contains four classes:

- `person`
- `car`
- `traffic light`
- `stop sign`

---

## 📁 Dataset Structure

Make sure your dataset is arranged in the following structure:

traffic_dataset/
├── images/
│ ├── train/
│ ├── val/
│ └── test/ 
├── labels/
│ ├── train/
│ ├── val/
│ └── test/
└── traffic_config.yaml


Each image must have a corresponding `.txt` file in the `labels/` folder, formatted in YOLO format:  
`<class_id> <x_center> <y_center> <width> <height>` — all normalized (0 to 1).

---

## 📝 Dataset Config (`traffic_config.yaml`)

```yaml
path: C:/Users/pandu/Pictures/traffic_dataset  # Update this to the root of your dataset

train: images/train
val: images/val
test: images/test  # Optional

names:
  0: person
  1: car
  2: traffic light
  3: stop sign
