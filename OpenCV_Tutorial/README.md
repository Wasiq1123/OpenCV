# 🧠 OpenCV_Tutorial

This repository contains a collection of Jupyter Notebooks to understand and implement the fundamentals of image processing using **OpenCV in Python**. The focus is on both theoretical understanding and practical applications.

---

## 📁 Directory Structure

```

OpenCV\_Tutorial/

├── OpenCV Basic\_Image\_Enhancement\_Operations.ipynb

├── OpenCV Canny Edge Detection.ipynb

├── OpenCV Filter Color in Video.ipynb

├── OpenCV Find Co-ordinates of Contours.ipynb

├── OpenCV Image Enhancement.ipynb

├── OpenCV Image Reading, Channel Modification, and Region Editing.ipynb

├── OpenCV Image Transformation.ipynb

├── OpenCV Line and Circle Detection.ipynb

└── README.md

````

---

## 📌 Notebook Summaries

### 📘 `OpenCV Image Reading, Channel Modification, and Region Editing.ipynb`

✅ **Covers:**
- Loading image from a URL using `urllib`
- Decoding image data to NumPy array with OpenCV
- Resizing with `cv2.resize()`
- Splitting image into RGB channels and modifying each
- Increasing brightness and clipping pixel values
- Changing pixel values in a specific region
- Cropping and displaying image sub-regions
- Adding brightness using numpy broadcasting
- Checking max pixel intensity

🧪 **Functions & Methods Used:**
```python
cv2.imdecode(), cv2.resize(), cv2.split(), cv2.merge()
np.clip(), np.add(), cv2.cvtColor(), cv2_imshow()
````

---

### 📘 `OpenCV Image Transformation.ipynb`

✅ **Covers:**

* **Translation**: Moving image using a transformation matrix
* **Rotation**: Rotating image about its center using `cv2.getRotationMatrix2D()`
* **Shearing**: Applying shear along x and y axis with custom matrix
* **Scaling**: Enlarging image using scaling factors

📌 Example:

```python
# Translation matrix
M = np.array([[1, 0, tx], [0, 1, ty]], dtype=np.float32)
translated = cv2.warpAffine(image, M, (width, height))
```

---

### 📘 `OpenCV Line and Circle Detection.ipynb`

✅ **Covers:**

* **Canny Edge Detection** as preprocessing
* **Hough Line Transform** to detect straight lines
* **Hough Circle Transform** to detect circular shapes
* Frame flipping for visualization
* Drawing detected shapes using `cv2.line()` and `cv2.circle()`

📌 Concepts Explained:

* Polar coordinate line representation (rho, theta)
* Why large constants like ±1000 are used for drawing full lines
* Accumulator resolution and thresholds in `cv2.HoughCircles()`

---

### 📘 `OpenCV Canny Edge Detection.ipynb`

✅ **Covers:**

* Edge detection using `cv2.Canny()`
* Adjusting thresholds for better edge quality
* Displaying grayscale and edge images side-by-side

---

### 📘 `OpenCV Filter Color in Video.ipynb`

✅ **Covers:**

* Capturing video stream
* Filtering specific color ranges using HSV masking
* Drawing contours on color-filtered objects
* Real-time visualization with OpenCV

---

### 📘 `OpenCV Find Co-ordinates of Contours.ipynb`

✅ **Covers:**

* Converting image to binary
* Detecting object boundaries using `cv2.findContours()`
* Drawing and labeling contours
* Getting exact (x, y) coordinates of each contour point

---

### 📘 `OpenCV Image Enhancement.ipynb`

✅ **Covers:**

* Brightness and contrast manipulation
* Histogram equalization for grayscale and color images
* Using CLAHE (Contrast Limited Adaptive Histogram Equalization)

---

### 📘 `OpenCV Basic_Image_Enhancement_Operations.ipynb`

✅ **Covers:**

* Basic operations like:

  * Pixel-wise addition
  * Subtraction
  * Multiplication
  * Logical operations on masks
* Image blending and arithmetic

---

## ✍️ Author

**Wasiq Saleem**
Student at NUST (Pakistan) | Robotics + Computer Vision Researcher
📍 Islamabad
🛠️ Skills: OpenCV, ROS 2, Python, Image Processing, AI

---

## 🔗 Dependencies

All notebooks require:

* Python 3.x
* OpenCV (`cv2`)
* NumPy
* Google Colab for `cv2_imshow()`

To install locally:

```bash
pip install opencv-python numpy
```

---

## 🚀 Run This Notebook on Colab

Click the badge below to launch the notebooks directly in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)

---

## 📌 License

This repository is shared for educational purposes. Free to use with proper attribution.
© 2025 Wasiq Saleem

---
