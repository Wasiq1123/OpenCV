## 🧠 OpenCV Tutorial – Image Processing & Computer Vision Essentials

This repository contains a series of hands-on projects and tutorials demonstrating **fundamental image processing techniques** using **OpenCV**. These notebooks are ideal for learning the basics of computer vision — including image enhancement, edge detection, geometric transformations, and object detection.

---

## 📂 Project Structure

```
📁 OpenCV_Basics
├── OpenCV Basic_Image_Enhancement_Operations.ipynb        # 🔧 Contrast, Brightness, Blurring
├── OpenCV Canny Edge Detection.ipynb                      # ⚡ Canny edge detection on images
├── OpenCV Filter Color in Video.ipynb                     # 🎥 Real-time color filtering in video
├── OpenCV Find Co-ordinates of Contours .ipynb            # 🌀 Contour detection & coordinate extraction
├── OpenCV Image Enhancement.ipynb                         # 🔬 Histogram Equalization, CLAHE
├── OpenCV Image Reading, Channel Modification...ipynb     # 📸 Channel-wise operations & region masking
├── OpenCV Image Transformation.ipynb                      # 🔄 Affine, rotation, translation, resizing
├── OpenCV Line and Circle Detection.ipynb                 # 🎯 Hough Transform for line/circle detection
├── README.md
```

---

## 🔍 Notebook Overviews

### 📸 **OpenCV Image Reading, Channel Modification, and Region Editing**

* Load, display, and modify RGB channels
* Apply masking and ROI (Region of Interest)
* Save processed images

---

### 🎨 **OpenCV Basic Image Enhancement Operations**

* Adjust brightness and contrast
* Apply Gaussian and median blurs
* Perform sharpening and smoothing

---

### 🌈 **OpenCV Image Enhancement**

* Histogram Equalization
* CLAHE (Contrast Limited Adaptive Histogram Equalization)
* Improves contrast and brightness adaptively

---

### 🧪 **OpenCV Canny Edge Detection**

* Detects sharp intensity changes using:

  * Gaussian blur
  * Gradient thresholding
* Ideal for edge-based segmentation

---

### 🌀 **OpenCV Find Coordinates of Contours**

* Detect shapes and extract contour points
* Find area, perimeter, and bounding boxes
* Useful for shape analysis and object localization

---

### 🔄 **OpenCV Image Transformation**

* Resize, scale, rotate, and translate images
* Includes affine and perspective transformations
* Core for geometric manipulation tasks

---

### 🎯 **OpenCV Line and Circle Detection**

* Uses Hough Line & Hough Circle Transforms
* Visualizes shapes over real-world objects
* Used in lane detection, object tracking

---

### 🎥 **OpenCV Filter Color in Video**

* Real-time object tracking using color masks
* Track red, green, blue, or custom HSV ranges
* Useful in gesture recognition, robotics vision

---

## 💻 Requirements

Install required libraries:

```bash
pip install opencv-python numpy matplotlib
```

Or in Google Colab:

```python
!pip install opencv-python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

---

## 🚀 Learning Outcomes

✔️ Read, display, and modify images and video streams

✔️ Apply fundamental filters: blurring, sharpening, edge detection

✔️ Perform color space filtering in video (HSV masking)

✔️ Transform images geometrically (rotate, resize, affine)

✔️ Detect contours, lines, and circles

✔️ Build a solid base for advanced computer vision tasks

---

## 🔗 Useful Resources

* 📘 [OpenCV-Python Documentation](https://docs.opencv.org/4.x/d6/d00/tutorial_py_root.html)
* 📺 [FreeCodeCamp OpenCV Tutorial](https://www.youtube.com/watch?v=oXlwWbU8l2o)
* 🧠 [PyImageSearch](https://pyimagesearch.com/)

---
