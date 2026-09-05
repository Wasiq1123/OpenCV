# OpenCV Computer Vision Fundamentals

![Python](https://img.shields.io/badge/Python-3.8+-blue)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?logo=opencv&logoColor=white)
![Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?logo=googlecolab&logoColor=white)

A structured set of Python/OpenCV notebooks covering classical image processing fundamentals, plus three real-time face detection/tracking pipelines (Haar Cascade, CSRT, MTCNN) with a side-by-side comparison of the three approaches.

## Contents

- [Repository Structure](#repository-structure)
- [What This Repository Covers](#what-this-repository-covers)
- [Tools & Frameworks](#tools--frameworks)
- [How the Projects Were Built](#how-the-projects-were-built)

## Repository Structure

```
opencv-cv-fundamentals/
│
├── OpenCV_Tutorial/        # Image processing fundamentals
│   ├── Image reading, channel modification, region editing
│   ├── Image transformation (translation, rotation, shear, scaling)
│   ├── Basic image enhancement operations (arithmetic, thresholding, bitwise ops)
│   ├── Image enhancement (brightness/contrast)
│   ├── Canny edge detection
│   ├── Line and circle detection (Hough transform)
│   ├── Color filtering in video (HSV masking)
│   └── Contour detection & coordinate extraction
│
├── OpenCV_Projects/         # Applied face detection/tracking pipelines
│   ├── Face and eye detection (Haar Cascade)
│   ├── Face tracking (CSRT)
│   └── Face detection (MTCNN)
│
└── README.md
```

Each folder has its own README with notebook-by-notebook details:

| Folder | Focus |
|---|---|
| [OpenCV_Tutorial](OpenCV_Tutorial/README.md) | Classical image processing fundamentals |
| [OpenCV_Projects](OpenCV_Projects/README.md) | Face detection & tracking pipelines |

## What This Repository Covers

- **Image Processing Fundamentals** — pixel-level operations (arithmetic, masking, bitwise logic), geometric transforms (translation, rotation, shear, scaling), thresholding (simple and adaptive), histogram-based enhancement, edge detection, Hough-based line/circle detection, HSV color filtering, and contour extraction.
- **Face Detection & Tracking** — three distinct approaches to finding and following a face across video frames: a classical feature-based detector (Haar Cascade), a detector-initialized tracker (CSRT), and a deep-learning-based detector (MTCNN) — implemented separately and compared directly.

## Tools & Frameworks

| Category | Tools |
|---|---|
| Core Library | OpenCV (`cv2`) |
| Supporting Libraries | NumPy, Matplotlib, `urllib` |
| Deep Learning Detector | MTCNN (Multi-task Cascaded CNN) |
| Environment | Google Colab, using `cv2_imshow` in place of `cv2.imshow` |

## How the Projects Were Built

The tutorial notebooks each isolate a single image-processing concept — reading in an image or video, applying one or two specific OpenCV operations, and displaying the result — so each technique can be understood on its own. The project notebooks follow a consistent pipeline: read a video frame by frame, run a detector (or a detector + tracker), draw the results, and display the annotated frame in real time.
