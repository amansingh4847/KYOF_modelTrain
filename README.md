# 🍽️ KYOF – Know Your Own Food (AI Model)

## Overview

KYOF (Know Your Own Food) is an AI-powered food detection system built using YOLOv8.
This project detects Indian food items like **Idli, Dosa, Banana, Chapati, Orange, Chutney**, etc., from images.

---

## 🧠 Model Details

* **Framework:** YOLOv8 (Ultralytics)
* **Model Type:** Object Detection
* **Base Model:** yolov8n.pt (Nano)
* **Training Device:** CPU
* **Epochs:** 30
* **Image Size:** 640x640

---

## 📊 Performance Metrics

| Metric    | Value    |
| --------- | -------- |
| mAP@50    | ~0.89 🔥 |
| mAP@50-95 | ~0.67 👍 |

👉 Model performs well on most food categories, with strong accuracy on **Idli, Dosa, and Orange**.

---

## 📁 Project Structure

```
KYOF_dataset.yolov8/
│── train/
│── valid/
│── test/
│── data.yaml
│
runs/
└── detect/
    └── train/
        └── weights/
            ├── best.pt   # ✅ Final trained model
            └── last.pt
```

---

## ⚙️ Installation

```bash
pip install ultralytics
```

---

## 🧪 How to Run Detection

```bash
yolo task=detect mode=predict model=runs/detect/train/weights/best.pt source="image.jpg"
```

👉 Replace `image.jpg` with your test image.

---

## 📸 Output

* Bounding boxes around detected food
* Class labels (e.g., idli, dosa)
* Confidence score

---

## 🧠 Dataset Info

* Total Images: ~1100+
* Train: ~942
* Validation: ~153
* Multiple Indian food classes

---

## 🚧 Future Improvements

* Increase dataset size for better generalization
* Improve low-performing classes (e.g., chutney)
* Convert model to **TensorFlow Lite (.tflite)** for mobile deployment
* Integrate into Flutter app (KYOF)

---

## 📱 Upcoming

This model will be integrated into a Flutter app for real-time food detection using the camera.

---

## 👨‍💻 Author

Developed by Aman 

---

## ⭐ Support

If you like this project, give it a ⭐ on GitHub!
