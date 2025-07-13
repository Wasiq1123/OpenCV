# 🔍 OpenCV

Welcome to the **OpenCV** repository — a structured collection of hands-on notebooks to learn and apply computer vision using **Python + OpenCV**.

This repository is organized into two main sections:
- 📘 `OpenCV_Tutorial`: Foundational tutorials for image processing and enhancement.
- 🚀 `OpenCV_Project`: Practical projects for face recognition, object tracking, and more.

---

## 📁 Folder Structure

```

OpenCV/
├── OpenCV_Tutorial/       # Step-by-step tutorials

│   ├── OpenCV Basic\_Image\_Enhancement\_Operations.ipynb

│   ├── OpenCV Canny Edge Detection.ipynb

│   ├── OpenCV Filter Color in Video.ipynb

│   ├── OpenCV Find Co-ordinates of Contours.ipynb

│   ├── OpenCV Image Enhancement.ipynb

│   ├── OpenCV Image Reading, Channel Modification, and Region Editing.ipynb

│   ├── OpenCV Image Transformation.ipynb

│   ├── OpenCV Line and Circle Detection.ipynb

│   └── README.md

│

├── OpenCV_Project/        # Real-world applications

│   ├── OpenCV Face and Eye Recognition.ipynb

│   ├── OpenCV Object Tracking.ipynb

│   ├── OpenCV and MTCNN Face Recognition.ipynb

│   └── README.md

│

└── README.md              # This file (Main Overview)

````

---

## 📘 OpenCV_Tutorial

Learn core image processing techniques step-by-step. These tutorials help build intuition and hands-on skills for:

- 📥 Reading and writing images
- 🎨 Color channel manipulation (RGB, HSV)
- 🔄 Image transformations: translation, rotation, scaling, shearing
- 🌈 Brightness and contrast enhancement
- 🖼️ Region-of-interest (ROI) selection and editing
- ✏️ Drawing shapes and text on images
- 🧠 Canny Edge Detection
- 🧵 Line & Circle detection using Hough Transform
- 🎯 Filtering specific colors in video frames

📎 [See full tutorial list → OpenCV_Tutorial/README.md](./OpenCV_Tutorial/README.md)

---

## 🚀 OpenCV_Project

This section contains complete applied projects demonstrating real-world applications of OpenCV, such as:

| Notebook | Description |
|----------|-------------|
| 🧠 `OpenCV Face and Eye Recognition.ipynb` | Detects human faces and eyes using Haar cascades |
| 🎯 `OpenCV Object Tracking.ipynb` | Tracks objects in video using OpenCV tracking APIs (KCF, CSRT, etc.) |
| 🤖 `OpenCV and MTCNN Face Recognition.ipynb` | Uses MTCNN for robust face detection with facial landmarks |

📎 [See project descriptions → OpenCV_Project/README.md](./OpenCV_Project/README.md)

---

## ⚙️ Setup & Installation

Make sure you have Python 3.x installed. Then install required libraries:

```bash
pip install opencv-python numpy matplotlib
````

For advanced face detection with MTCNN:

```bash
pip install facenet-pytorch
```

> ✅ All notebooks are tested and runnable on Google Colab.
> Use `cv2_imshow` (not `cv2.imshow`) for displaying images in Colab.

---

## ✅ Highlights

* Modular & well-commented Jupyter notebooks
* Easy-to-understand explanations for each image operation
* Visual outputs for every processing step
* MTCNN integration for deep face recognition

---

## 📜 License

This repository is open-source and intended for **educational and research purposes**.
You are free to modify, reuse, and share — **with attribution**.
