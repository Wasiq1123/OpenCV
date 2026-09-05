# OpenCV Projects — Face Detection & Tracking

Three real-time face detection/tracking pipelines applied to video: a classical feature-based detector, a detector-initialized tracker, and a deep-learning-based detector — implemented separately so their behavior can be compared directly.

## Notebooks

| Notebook | Method | Type |
|---|---|---|
| `OpenCV Face and Eye Recognition.ipynb` | Haar Cascade | Classical, feature-based detection |
| `OpenCV Object Tracking.ipynb` | Haar Cascade + CSRT | Detection-initialized tracking |
| `OpenCV and MTCNN Face Recognition.ipynb` | MTCNN | Deep-learning-based detection |

---

## Face and Eye Detection (Haar Cascade)

- Uses `cv2.CascadeClassifier` with the pretrained `haarcascade_frontalface_default.xml` and `haarcascade_eye.xml` models
- For every video frame: detects faces on the grayscale frame with `detectMultiScale` (`scaleFactor=1.1`, `minNeighbors=5`, `minSize=(30,30)`), then searches for eyes within each detected face's region of interest
- Draws face boxes in blue and eye boxes in green

## Object Tracking (CSRT)

- Detects an initial face with the same Haar Cascade classifier
- On first detection, initializes `cv2.TrackerCSRT_create()` on the detected face region
- On every subsequent frame, updates the tracker directly (`tracker.update(frame)`) instead of re-running detection — maintaining a bounding box even as the face moves
- If tracking fails, the tracker is reset to `None` so detection runs again on the next frame

## Face Detection (MTCNN)

- Uses the `MTCNN` Python package (`from mtcnn import MTCNN`) to detect faces directly, without Haar features
- For every video frame: runs `detector.detect_faces(frame)` and draws a bounding box for each detected face

## Comparison of Techniques

| Feature | Haar Cascade | CSRT Tracker | MTCNN |
|---|---|---|---|
| Detection method | Feature-based | Tracker after initial detection | Deep CNN-based |
| Real-time performance | Fast | Real-time capable | Slower |
| Robust to angle & lighting | No | Limited | Yes |
| Eye detection support | Yes (built-in) | No | No (face only) |

## Requirements

```bash
pip install opencv-python mtcnn
```

Haar cascade XML files are pulled directly from the OpenCV repository:

```bash
wget https://github.com/opencv/opencv/raw/master/data/haarcascades/haarcascade_frontalface_default.xml
wget https://github.com/opencv/opencv/raw/master/data/haarcascades/haarcascade_eye.xml
```

All notebooks are written for Google Colab and use `cv2_imshow()` in place of `cv2.imshow()`.
