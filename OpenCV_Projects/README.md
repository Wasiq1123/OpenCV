## 🧠 Real-Time Face Detection & Tracking with OpenCV, Haar Cascades, CSRT, and MTCNN

This repository contains multiple practical implementations of **real-time face detection and tracking** techniques using OpenCV and deep learning-based MTCNN in Google Colab. It covers various stages of face detection pipelines such as:

* Frame extraction and transformation
* Face and eye detection with Haar Cascades
* Real-time object tracking using CSRT
* Face detection using MTCNN (Multi-task Cascaded Convolutional Neural Network)

---

## 📁 Project Structure

```
📁 Face_Detection_Tracking

├── HaarCascade_Face_Eye_Detection.ipynb       # Face & eye detection using Haar cascades

├── Face_Tracking_with_CSRT.ipynb              # Tracking faces with OpenCV CSRT tracker

├── MTCNN_Face_Detection.ipynb                 # Deep learning-based face detection with MTCNN

├── haarcascade_frontalface_default.xml        # XML file for frontal face detection

├── haarcascade_eye.xml                        # XML file for eye detection

└── README.md
```

---

## 🔍 Implementation Overview

### ✅ 1. **Face and Eye Detection using Haar Cascades**

* Uses OpenCV’s `CascadeClassifier` to detect:

  * Faces using `haarcascade_frontalface_default.xml`
  * Eyes using `haarcascade_eye.xml`

* Real-time bounding boxes:

  * Blue for faces
  * Green for eyes

📌 Ideal for lightweight face detection where speed is important.

---

### ✅ 2. **Face Tracking with CSRT Tracker**

* Initially detects the face using Haar Cascade.
* Initializes a `cv2.TrackerCSRT_create()` object to follow the face across frames.
* Updates position even if face detection fails after first frame.

📌 Great for **persistent tracking** in real-time video streams even when the face moves or is momentarily occluded.

---

### ✅ 3. **Face Detection with MTCNN**

* Implements face detection using the deep learning-based **MTCNN** (Multi-task Cascaded Convolutional Neural Networks).
* Uses the `MTCNN` Python package.
* Detects faces directly without requiring Haar features.

📌 More robust to scale, lighting, and angle variations than traditional methods.

---

## 🧪 Comparison of Techniques

| Feature                    | Haar Cascade    | CSRT Tracker          | MTCNN                   |
| -------------------------- | --------------- | --------------------- | ----------------------- |
| Detection Method           | Feature-based   | Tracker after initial | Deep CNN-based          |
| Real-Time Performance      | ✅ Fast          | ✅ Real-time capable   | ⚠️ Slightly slower      |
| Robust to Angle & Lighting | ❌ No            | ❌ Limited             | ✅ Yes                   |
| Eye Detection Support      | ✅ Built-in      | ❌ No                  | ✅ Face only (no eye)    |
| Use Case                   | Basic Detection | Object Tracking       | Advanced Face Detection |

---

## 💻 Setup Instructions

### ✅ In Google Colab

```python
from google.colab import drive
drive.mount('/content/drive')
```

### ✅ Install Dependencies

```bash
!pip install mtcnn opencv-python
```

### ✅ Download Haar Cascades

```bash
!wget https://github.com/opencv/opencv/raw/master/data/haarcascades/haarcascade_frontalface_default.xml

!wget https://github.com/opencv/opencv/raw/master/data/haarcascades/haarcascade_eye.xml
```

---

## 🎯 Real-World Applications

✔️ Security surveillance with live video feeds

✔️ Real-time face tracking in robotic vision systems

✔️ Attendance systems using webcams

✔️ Human-computer interaction & gaze tracking

✔️ Video analytics for sports, events, or retail

---

## 📌 Key Learning Highlights

* 🎥 Read and process frames from video files or webcams
* 🔄 Flip, convert color spaces, and extract grayscale
* 👀 Detect multiple facial landmarks and ROIs
* 🎯 Use trackers to follow moving faces over time
* 🧠 Understand the difference between classical and deep learning-based detection

---

