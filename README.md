# Applied Computer Vision with OpenCV: Fundamentals, Face Detection, and Tracking

A structured set of Python/OpenCV notebooks covering classical image processing fundamentals and three face detection/tracking pipelines (Haar Cascade, CSRT, MTCNN), including a side-by-side comparison of detection methods.

This repository documents foundational computer vision work: understanding of core image processing operations and practical application of classical and deep-learning-based face detection/tracking methods.

## Scope

| In this repo |
|---|
| Classical image processing (transformations, filtering, edge/contour/line detection, histogram methods) |
| Application of pretrained/classical detectors (Haar Cascade, MTCNN) and a built-in tracker (CSRT) |
| Qualitative comparison of three face detection/tracking approaches |
| Google Colab notebooks, runnable end-to-end |

## Repository Structure

```
OpenCV/
├── OpenCV_Tutorial/        Image processing fundamentals
│   ├── Image reading, channel modification, region editing
│   ├── Image transformation (translation, rotation, shear, scaling)
│   ├── Basic image enhancement operations (arithmetic, masking)
│   ├── Image enhancement (brightness/contrast, histogram equalization, CLAHE)
│   ├── Canny edge detection
│   ├── Line and circle detection (Hough transform)
│   └── Color filtering in video (HSV masking)
│
├── OpenCV_Projects/        Applied face detection/tracking pipelines
│   ├── Face and eye detection (Haar Cascade)
│   ├── Object/face tracking (CSRT)
│   └── Face detection with MTCNN
│
└── README.md
```

## Tutorial Notebooks

| Notebook | Core operations |
|---|---|
| Image Reading, Channel Modification, and Region Editing | `cv2.imdecode`, `cv2.resize`, channel split/merge, ROI editing, brightness clipping |
| Image Transformation | Affine transforms via `cv2.warpAffine` — translation, rotation, shear, scaling |
| Basic Image Enhancement Operations | Pixel-wise arithmetic, masking, image blending |
| Image Enhancement | Brightness/contrast adjustment, histogram equalization, CLAHE |
| Canny Edge Detection | `cv2.Canny`, threshold tuning |
| Line and Circle Detection | Hough Line and Hough Circle transforms |
| Filter Color in Video | HSV color-range masking, contour drawing on filtered regions |
| Find Co-ordinates of Contours | `cv2.findContours`, contour labeling and coordinate extraction |

## Face Detection and Tracking Pipelines

Three approaches to face detection/tracking are implemented and compared directly:

| Method | Type | Real-time performance | Robust to angle/lighting | Eye detection |
|---|---|---|---|---|
| Haar Cascade | Classical, feature-based | Fast | No | Yes (built-in) |
| CSRT Tracker | Detection + tracking (Haar init) | Real-time capable | Limited | No |
| MTCNN | Deep learning (CNN cascade) | Slower | Yes | No (face only) |

- **Haar Cascade** uses `cv2.CascadeClassifier` with pretrained XML models for frontal face and eye detection.
- **CSRT** initializes on a Haar-detected face, then uses `cv2.TrackerCSRT_create()` to maintain tracking across frames without re-running detection each frame.
- **MTCNN** applies a pretrained multi-task cascaded CNN for detection that is more robust to scale, angle, and lighting variation than Haar-based methods.

## Setup

```bash
pip install opencv-python numpy matplotlib mtcnn
```

Haar cascade XML files are pulled directly from the OpenCV repository:
```bash
wget https://github.com/opencv/opencv/raw/master/data/haarcascades/haarcascade_frontalface_default.xml
wget https://github.com/opencv/opencv/raw/master/data/haarcascades/haarcascade_eye.xml
```

All notebooks are written for Google Colab and use `cv2_imshow` in place of `cv2.imshow`.

## License

Shared for educational and research purposes. Free to use and modify with attribution.
© 2025 Muhammad Wasiq Saleem
