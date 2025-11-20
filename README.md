
<div align="center">

# 🧠 Fetal Brain Abnormalities Detection  
### Using Deep Learning, YOLOv5, and Ultrasound Imaging

A complete end-to-end system for detecting **fetal brain abnormalities** from ultrasound images using **YOLOv5**, **Python**, **OpenCV**, and a **Flask web interface**.

</div>

---

## 🏆 Overview

This project aims to assist **early diagnosis** of fetal brain abnormalities by providing an automated, fast, and accurate computer-vision–based detection system.

✔ Trained on a **Roboflow fetal-brain dataset** (1391 images)  
✔ Real-time detection using YOLOv5  
✔ Web dashboard for uploading & analyzing ultrasound images  
✔ SQLite-based user authentication system  
✔ Automatic before/after comparison visualization  

---

## 🚀 Features

- 🧠 **YOLOv5-based abnormality detection**
- ⚡ **Real-time inference** via Flask
- 📊 **Preprocessed ultrasound dataset**
- 🖼️ **Bounding-box visualization**
- 👤 **User Login/Registration**
- 💾 **Results automatically saved**
- 🔧 **Easy to deploy & extend**

---

## 📁 Project Structure

```
.
├── app.py                # Flask web server
├── detect.py             # YOLOv5 detection logic
├── train.py              # YOLOv5 training module
├── val.py                # Model validation
├── export.py             # Export to ONNX/TFLite/CoreML
├── requirements.txt      # Dependencies
├── best.pt               # Trained YOLOv5 model weights
├── static/
│   ├── test/             # Input images
│   └── result/           # Output images with boxes
└── templates/
    ├── index.html        # Login page
    └── userlog.html      # Upload & analysis dashboard
```

---

## 🔬 Dataset Details

- **Source:** Roboflow Universe  
- **Images:** 1391 ultrasound images  
- **Format:** YOLOv5  
- **Pre-processing:**  
  - Auto-orientation  
  - Resize to **640×640**  
  - Annotations included  

---

## 🧠 Model Training

To train the YOLOv5 model with your dataset:

```bash
python train.py --data data.yaml --weights yolov5s.pt --img 640 --epochs 50
```

You may use YOLOv5 pre-trained weights or train from scratch.

---

## 🔍 Running Inference (CLI)

```bash
python detect.py --weights best.pt --source path/to/image.jpg
```

Detection results are saved under:

```
runs/detect/exp/
```

---

## 🌐 Running the Web App

### 1️⃣ Install dependencies
```bash
pip install -r requirements.txt
```

### 2️⃣ Start Flask server
```bash
python app.py
```

### 3️⃣ Open browser
```
http://127.0.0.1:5000/
```

### Web Features
- Upload an ultrasound image  
- Backend runs YOLOv5 detection  
- Shows **original** and **detected** image side-by-side  
- Saves results for review  

---

## 📸 Sample Workflow

1. **User uploads ultrasound scan**  
2. **Model detects abnormalities**  
3. **Bounding boxes are drawn**  
4. **Results displayed instantly**  
5. **Image saved to /static/result**  

---

## 🛠️ Tech Stack

| Component | Technology |
|----------|------------|
| Model | YOLOv5, PyTorch |
| Language | Python |
| CV Library | OpenCV |
| Web Framework | Flask |
| Database | SQLite |
| Frontend | HTML, CSS |

---

## 🚀 Future Enhancements

- Add classification probability charts  
- Support DICOM images  
- Add multi-class abnormality detection  
- Deploy on cloud (AWS / Render / HuggingFace Spaces)  
- Mobile-friendly UI  

---

## 🤝 Contributing

Pull requests and issue reports are welcome!  
Feel free to fork this repo and enhance the model or UI.

---

## 📜 License

This project is for educational and research purposes.

---

## ⭐ Support

If you found this project useful, please consider giving a **star ⭐ on GitHub**!

---

<div align="center">

### Made with ❤️ using Python, Deep Learning, and Ultrasound AI

</div>
