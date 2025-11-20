# 🧠 Fetal Brain Abnormalities Detection

### Deep Learning • YOLOv5 • Ultrasound Imaging • Flask Web App

This repository contains a complete end-to-end system for detecting **fetal brain abnormalities** from ultrasound images using **YOLOv5**, **Python**, **OpenCV**, and a **Flask-based web interface**.

The goal is to support **early diagnosis** by enabling automated detection of abnormalities in fetal brain ultrasound scans.

---

<div align="center">

### ⭐ Technologies Used

**Python · YOLOv5 · OpenCV · Flask · SQLite · Roboflow Dataset · Deep Learning**

</div>

---

## 📌 Features

* 🧠 **YOLOv5-based detection** of fetal brain abnormalities
* ⚡ **Real-time inference** through a Flask web dashboard
* 📝 **User authentication system** (SQLite)
* 🖼️ Upload ultrasound images for instant prediction
* 🔍 Bounding box visualization on detected anomalies
* 💾 Auto-save of test images & results
* 🔧 Fully customizable and extendable architecture

---

## 📁 Project Structure (Matches Your GitHub Repo)

```
.
├── __pycache__/              # Python cache files
├── datasets/                 # Dataset folder (Roboflow dataset files)
├── models/                   # YOLO model configuration files
├── result/                   # Detection outputs (if saved manually)
├── runs/
│   └── detect/               # YOLOv5 detection run outputs
├── segment/                  # Segmentation-related files (if used)
├── static/                   
│   ├── test/                 # User-uploaded input images
│   └── result/               # Output images after detection
├── templates/
│   ├── index.html            # Login / Register page
│   └── userlog.html          # Analysis dashboard
├── utils/                    # YOLO utility scripts
│
├── README.dataset.txt        # Dataset summary
├── README.roboflow.txt       # Roboflow export details
├── README.md                 # Project documentation
│
├── app.py                    # Flask backend
├── best.pt                   # Trained YOLOv5 model weights
├── detect.py                 # Object detection script
├── export.py                 # Export model to ONNX / TFLite
├── requirements.txt          # Python dependencies
├── train.py                  # Model training script
├── tutorial.ipynb            # Jupyter Notebook for testing/analysis
├── user_data.db              # SQLite User database
└── val.py                    # Validation script
```

---

## 📊 Dataset Information

* **Source:** Roboflow Universe
* **Total Images:** *1391 fetal brain ultrasound images*
* **Annotation Format:** YOLOv5 (Bounding boxes)
* **Preprocessing Applied:**

  * EXIF orientation correction
  * Resized to **640×640**
  * Auto-oriented pixel data

> The dataset is stored inside the `datasets/` directory.

---

## 🧠 Model Architecture (YOLOv5)

This project uses **YOLOv5** for object detection because of its:
✔ Fast inference
✔ High accuracy
✔ Ease of training on custom datasets

Training scripts (`train.py`, `val.py`) are included and fully configurable.

---

## 🚀 Training the Model

To retrain the model:

```bash
python train.py --data data.yaml --weights yolov5s.pt --img 640 --epochs 50
```

This will generate new weights inside:

```
runs/train/exp/weights/best.pt
```

---

## 🔍 Running YOLO Detection (CLI)

Detect abnormalities on a folder or single image:

```bash
python detect.py --weights best.pt --source static/test/
```

Output images will be saved under:

```
runs/detect/exp/
```

---

## 🌐 Running the Web Application

### 1️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 2️⃣ Launch Flask Server

```bash
python app.py
```

### 3️⃣ Visit the Web Portal

Open your browser:

```
http://127.0.0.1:5000/
```

### Web Features:

* Login / Register using SQLite
* Upload ultrasound image
* YOLO model generates detection
* Shows **Original Image vs Detected Image**
* Result saved in `static/result/`

---

## 🖼️ How It Works (Workflow)

1. Upload fetal ultrasound scan
2. Flask sends image to YOLO model
3. YOLOv5 performs detection
4. Bounding boxes drawn around abnormalities
5. Output displayed instantly
6. Images saved for review

---

## 🛠️ Tech Stack

| Component       | Technology      |
| --------------- | --------------- |
| Deep Learning   | YOLOv5, PyTorch |
| Computer Vision | OpenCV          |
| Web Framework   | Flask           |
| Backend         | Python          |
| Database        | SQLite          |
| Frontend        | HTML, CSS       |

---

## 🚀 Future Improvements

* Add support for **multi-class fetal abnormality detection**
* Deploy to **Render / Railway / AWS / HuggingFace Spaces**
* Convert to **ONNX or TFLite** for mobile deployment
* Add charts & detection confidence summary
* Add DICOM support (for medical imaging workflows)

---

## 🤝 Contributing

Contributions are welcome!
Fork the repo → Make improvements → Create a Pull Request.

---

## 📜 License

This project is intended for **research and educational purposes** only.
Not approved for clinical or diagnostic medical use.

---

<div align="center">

### ⭐ If you like this project, please give it a star on GitHub!

Built with ❤️ using Python, Deep Learning & Medical Imaging.

</div>

