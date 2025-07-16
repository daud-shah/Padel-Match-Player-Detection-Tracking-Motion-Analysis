# 🎾 Padel Match Player Detection, Tracking & Motion Analysis

![Python](https://img.shields.io/badge/Python-3.11+-blue)
![YOLO](https://img.shields.io/badge/YOLO-Ultralytics-red)
![OpenCV](https://img.shields.io/badge/OpenCV-4.5+-orange)
![License](https://img.shields.io/badge/License-MIT-yellow)

A computer vision system that detects and tracks players in **padel match videos** using YOLOv8 and Deep SORT. The system supports real-time detection, unique player ID tracking, and sets the foundation for motion analytics like speed and movement heatmaps.

---

## 🌟 Features

- ⚡ Real-time **player detection** with YOLOv8/YOLOv11
- 🛰️ Multi-object tracking using **Deep SORT**
- 📈 Motion tracking for movement analysis
- 🎥 Video input/output with bounding box overlays
- 📦 Easy integration with Roboflow datasets

---

## 🛠️ Installation

1. **Clone the repository**:

   git clone https://github.com/yourusername/padel-player-tracking.git
   cd padel-player-tracking


2. **Install dependencies**:

   pip install ultralytics<=8.3.40 deep-sort-realtime opencv-python supervision roboflow
   

3. **Download model weights**:

   * Add your trained YOLO weights (`best.pt`) in the project root

---

## 🚀 Usage

### Process a padel match video:


python track_players.py --input match.mp4 --output output.mp4


### Optional arguments:

* `--model`: Path to custom YOLO weights (`best.pt`)
* `--conf`: Confidence threshold (default: 0.25)
* `--device`: Use `0` for GPU or `'cpu'` for CPU

### Example code:

```python
from ultralytics import YOLO
from deep_sort_realtime.deepsort_tracker import DeepSort

# Load YOLOv8 model
model = YOLO("best.pt")

# Run inference
results = model("padel_frame.jpg", conf=0.25)
results[0].show()  # Show bounding boxes
```

---

## 📂 Project Structure


padel-player-tracking/
├── track_players.py      # Main video processing script
├── best.pt               # Trained YOLOv8 model
├── input/                # Raw input match videos
├── output/               # Annotated result videos
├── utils/                # Helper functions
└── README.md             # Project documentation


---

## 🧠 Detection Classes

| Class ID | Class Name | Description      |
| -------- | ---------- | ---------------- |
| 0        | Player     | Padel player     |
| 1        | Ball       | (Optional class) |

*Tracking is applied per player using Deep SORT, with unique ID for each.*

---

## ⚙️ System Pipeline

1. Extract video frames using OpenCV
2. Perform YOLOv8 detection on each frame
3. Pass detections to Deep SORT tracker
4. Draw bounding boxes with player ID
5. Write annotated frames to output video

---

## 🎯 Applications

* Sports Analytics & Strategy
* Player Movement Visualization
* Broadcast Enhancements
* Motion Heatmap & Speed Estimation *(coming soon)*

---

## 📈 Future Improvements

* [ ] Speed & Distance Analysis per Player
* [ ] Heatmap Generation
* [ ] Integration with Streamlit for UI
* [ ] Web Dashboard for Match Stats
* [ ] Referee Assistance System

---

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/new-feature`)
3. Commit your changes (`git commit -m 'Add new tracking logic'`)
4. Push to your branch (`git push origin feature/new-feature`)
5. Open a Pull Request

---

## 📜 License

Distributed under the MIT License. See `LICENSE` for details.

---

## 🔗 Connect with Me

* 💼 [LinkedIn](https://www.linkedin.com/in/daud-shah40)
* 🧠 AI Projects: [GitHub Portfolio](https://github.com/daud-shah)

---

> *“Detecting and tracking every move – one frame at a time.”*
