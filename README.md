# 🧠 OpenCV_Projects

This repository contains a complete collection of **OpenCV-based projects and tutorials** for learning and implementing computer vision techniques in Python.

Whether you're a beginner or intermediate learner, these notebooks will help you understand core image processing operations, facial recognition techniques, object tracking, and more — all powered by OpenCV and complementary libraries.

---

## 📁 Repository Structure

```

OpenCV\_Projects/
├── OpenCV Face and Eye Recognition.ipynb
├── OpenCV Object Tracking.ipynb
├── OpenCV and MTCNN Face Recognition .ipynb
├── OpenCV\_Tutorial/
│   ├── OpenCV Basic\_Image\_Enhancement\_Operations.ipynb
│   ├── OpenCV Canny Edge Detection.ipynb
│   ├── OpenCV Filter Color in Video.ipynb
│   ├── OpenCV Find Co-ordinates of Contours.ipynb
│   ├── OpenCV Image Enhancement.ipynb
│   ├── OpenCV Image Reading, Channel Modification, and Region Editing.ipynb
│   ├── OpenCV Image Transformation.ipynb
│   ├── OpenCV Line and Circle Detection.ipynb
│   └── README.md
├── README.md  ← (This file)

````

---

## 🔷 Main Projects

### 📘 `OpenCV Face and Eye Recognition.ipynb`
✅ Detects **faces and eyes** using Haar Cascade classifiers.

- Uses pre-trained Haar XML classifiers for detection.
- Converts frames to grayscale for performance.
- Highlights eyes and faces with bounding rectangles.
- Can be extended to work with live webcam input.

---

### 📘 `OpenCV and MTCNN Face Recognition.ipynb`
✅ Performs **face detection and alignment** using **MTCNN**.

- Uses **MTCNN (Multi-task Cascaded Convolutional Networks)** for more robust face detection than Haar cascades.
- Detects face bounding boxes and landmarks (eyes, nose, mouth).
- Suitable for further tasks like face recognition or verification.

📌 Dependencies:
- `facenet-pytorch` or `mtcnn` for face detection.
- OpenCV for image handling and visualization.

---

### 📘 `OpenCV Object Tracking.ipynb`
✅ Tracks moving objects using OpenCV’s tracking algorithms.

- Allows selection of a region (ROI) in video frames.
- Supports multiple trackers like KCF, CSRT, MOSSE.
- Can run on video files or live webcam stream.

---

## 📚 OpenCV_Tutorial (Fundamentals)

The `OpenCV_Tutorial/` folder contains step-by-step tutorials on the **core image processing techniques** used in OpenCV. Topics include:

| Notebook Title | Key Topics |
|----------------|------------|
| **Image Reading, Channel Modification, and Region Editing** | Read, resize, split channels, pixel manipulation |
| **Image Transformation** | Translate, rotate, shear, scale |
| **Line and Circle Detection** | Canny edges, HoughLines, HoughCircles |
| **Canny Edge Detection** | Grayscale conversion, edge detection |
| **Find Co-ordinates of Contours** | Contour detection, area, centroids |
| **Filter Color in Video** | Color masking using HSV space |
| **Image Enhancement** | Brightness, contrast, histogram equalization |
| **Basic Image Enhancement Operations** | Addition, subtraction, multiplication, blending |

📌 A separate [`README.md`](./OpenCV_Tutorial/README.md) is included inside the folder to guide you through each tutorial.

---

## 🚀 Getting Started

### ✅ Requirements

Install required libraries using:

```bash
pip install opencv-python numpy matplotlib
````

For MTCNN-related notebooks:

```bash
pip install facenet-pytorch
```

### 💻 Run on Google Colab (Recommended)

These notebooks are tested on **Google Colab** for free GPU/CPU support and easy visualization using `cv2_imshow`.

---

## 📄 License

This repository is licensed for **educational and personal learning**.
Feel free to use, modify, and build upon with attribution.

© 2025 Wasiq Saleem
