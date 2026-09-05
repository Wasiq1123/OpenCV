# OpenCV Tutorial — Image Processing Fundamentals

Eight notebooks covering the building blocks of classical image processing: reading and manipulating images, geometric transforms, enhancement, edge/line/circle detection, color filtering, and contour extraction.

## Notebooks

| Notebook | Core operations |
|---|---|
| `OpenCV Image Reading, Channel Modification, and Region Editing.ipynb` | Loading images from a URL, channel split/merge, ROI editing, brightness clipping |
| `OpenCV Image Transformation.ipynb` | Affine transforms via `cv2.warpAffine` — translation, rotation, shear, scaling |
| `OpenCV Basic_Image_Enhancement_Operations.ipynb` | Pixel-wise arithmetic, thresholding, bitwise operations |
| `OpenCV Image Enhancement.ipynb` | Brightness/contrast adjustment via pixel-wise add/multiply |
| `OpenCV Canny Edge Detection.ipynb` | `cv2.Canny` edge detection on video |
| `OpenCV Line and Circle Detection.ipynb` | Hough Line and Hough Circle transforms |
| `OpenCV Filter Color in Video.ipynb` | HSV color-range masking on live video |
| `OpenCV Find Co-ordinates of Contours.ipynb` | `cv2.findContours`, contour approximation and coordinate labeling |

---

## Image Reading, Channel Modification, and Region Editing

- Downloads an image directly from a URL (`urllib.request`), decodes it with `cv2.imdecode`, and resizes it with `cv2.resize`
- Splits the image into individual channels with `cv2.split`, brightens each channel independently, then recombines them with `cv2.merge`
- Edits a specific rectangular region of the image directly through NumPy slicing, and crops a sub-region for display
- Confirms pixel values stay within the valid `0–255` range using `np.clip`

**Example:** a `1080×810×3` source image is resized to `400×400` before channel-level editing.

## Image Transformation

Four affine transforms are applied to the same resized image using `cv2.warpAffine`:

| Transform | Parameters used |
|---|---|
| Translation | `tx = 50`, `ty = 50` |
| Rotation | 20°, scale factor 1, about the image center, via `cv2.getRotationMatrix2D` |
| Shear | shear factors `-0.15` (x) and `0.15` (y) |
| Scaling | 2× in both axes, with the output canvas enlarged to `800×800` |

## Basic Image Enhancement Operations

- Brightness adjustment via `np.add`/`np.subtract` with a constant offset, and contrast adjustment via `np.multiply` with scaling factors of `0.8`/`1.2`
- Simple thresholding (`cv2.threshold`, binary-inverse) and adaptive thresholding (`cv2.adaptiveThreshold`, Gaussian-weighted)
- Bitwise `AND`/`OR` operations between two different images (both resized to `400×400`) to illustrate mask-based compositing

## Image Enhancement

- Downloads a sample image bundle from a hosted zip archive and loads a `600×840×3` test image
- Demonstrates brightness changes with `cv2.add`/`cv2.subtract` against a constant-value image
- Demonstrates contrast changes with `cv2.multiply`, using factors of `1.2` (increase) and `0.8` (decrease)

## Canny Edge Detection

- Applies Gaussian blur, then `cv2.Canny` with thresholds `75`/`150`, frame by frame on a video, to extract edges in real time

## Line and Circle Detection

- **Line detection:** Canny edges (thresholds `100`/`200`) feed into `cv2.HoughLines` (`threshold=150`); detected lines are converted from polar (`rho`, `theta`) to two endpoints and drawn with `cv2.line`
- **Circle detection:** Gaussian-blurred frames feed into `cv2.HoughCircles` (`cv2.HOUGH_GRADIENT`, `param1=50`, `param2=30`), with detected circles drawn using `cv2.circle`

## Filter Color in Video

- Converts each video frame to HSV and applies `cv2.inRange` with a custom lower/upper HSV bound to isolate a specific color range
- Uses `cv2.bitwise_and` with the resulting mask to keep only the matching pixels, displayed in real time

## Find Co-ordinates of Contours

- Thresholds each frame (`cv2.threshold`, value `110`) and extracts contours with `cv2.findContours` (`RETR_TREE`, `CHAIN_APPROX_SIMPLE`)
- Simplifies each contour's shape with `cv2.approxPolyDP` and labels every vertex with its `(x, y)` pixel coordinates directly on the frame

## Requirements

```bash
pip install opencv-python numpy
```

All notebooks are written for Google Colab and use `cv2_imshow()` in place of `cv2.imshow()`.
