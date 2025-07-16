# 🎾 Padel Match Player Detection, Tracking & Motion Analysis

This project focuses on detecting and tracking players in a **padel match** using **YOLOv8/YOLOv11** for object detection and **Deep SORT** for multi-object tracking. It also lays the groundwork for future **motion analysis** such as player speed, movement paths, and heatmaps.

---

## 📌 Project Highlights

- 🎯 **Objective**: Detect and track padel players in match videos for sports analytics.
- ⚙️ **Technologies**: YOLOv11, Deep SORT, OpenCV, Roboflow
- 📹 **Input**: Custom-labeled video dataset of padel matches
- 🧠 **Output**: Real-time player detection & tracking with bounding boxes and player IDs

---

## 🚀 Tech Stack

| Component       | Tool/Library             |
|----------------|--------------------------|
| Object Detection | YOLOv8 / YOLOv11 (Ultralytics) |
| Tracking         | Deep SORT (Real-time)   |
| Data Annotation  | Roboflow                |
| Visualization    | OpenCV, Supervision     |
| Notebook         | Jupyter / Kaggle        |

---

## 📂 Folder Structure

```

📁 padel-match-tracking/
├── 📜 padel-player-detection.ipynb
├── 📁 dataset/
│   └── data.yaml, train/images, ...
├── 📁 runs/
│   └── train results, model weights
├── 📽️ input\_video.mp4
├── 📽️ output\_tracked\_video.avi
└── 📜 README.md

````

---

## 🔧 Installation

```bash
pip install -U ultralytics deep-sort-realtime opencv-python roboflow supervision
````

---

## 🧪 Training YOLO Model

```bash
yolo task=detect mode=train model=yolo11s.pt data="path/to/data.yaml" epochs=50 imgsz=640 batch=16
```

---

## 🛰️ Tracking with Deep SORT

Use Deep SORT with your YOLO detection output to track players frame-by-frame. The final output overlays bounding boxes and unique IDs for each player.

---

## 📊 Future Work

* Calculate **motion paths** of each player
* Generate **heatmaps** and **player speed**
* Build a **dashboard** for sports analytics

---

## 📽️ Demo

> [🎥 View Demo](#)

---

## 🤝 Let's Connect

If you’re interested in similar projects or need help with computer vision tasks like:

* Object Detection
* Player Tracking
* Custom Model Training

Feel free to connect with me on [LinkedIn]([https://www.linkedin.com/in/yourprofile](https://www.linkedin.com/in/daud-shah40))!

---

## 📌 License

MIT License

---

## 💬 Credits

* [Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics)
* [Deep SORT](https://github.com/mikel-brostrom/Yolov5_DeepSort_Pytorch)
* [Roboflow](https://roboflow.com/)

```

---

Would you like me to:
- Customize this with your GitHub username and links?
- Help you design a project **thumbnail** for the repo?

Let me know if you want to upload this to GitHub together.
```
