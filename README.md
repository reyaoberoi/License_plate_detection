# Image Processing for License Plate Recognition

## Overview

License Plate Recognition (LPR) is a key component of Intelligent Transportation Systems, enabling automated vehicle identification for applications such as traffic monitoring, toll collection, parking management, and law enforcement.
This project presents an end-to-end LPR pipeline using **classical image processing techniques combined with machine learning**, focusing on robustness under real-world conditions such as uneven lighting, noise, and perspective distortion.

---

## 🧠 Methodology

The proposed system follows a structured multi-stage pipeline:

1. **Image Preprocessing**

   * Grayscale conversion
   * Noise reduction
   * Contrast enhancement using Histogram Equalization & CLAHE

2. **License Plate Localization**

   * Adaptive thresholding
   * Canny edge detection
   * Contour detection and filtering based on geometric properties

3. **Character Segmentation**

   * Morphological operations
   * Contour-based character extraction
   * Sorting characters left-to-right

4. **Post-processing & Enhancement**

   * Plate alignment and rotation correction
   * Re-thresholding and image inversion for OCR readiness

5. **Character Recognition**

   * OCR using Tesseract
   * CNN-based character classification (A–Z, 0–9)

6. **Final Prediction**

   * Sequence reconstruction of detected characters
   * Overlay of predicted license plate on the original image

---

## 📊 Results

* **Accuracy:** 85–90% (OpenCV + Tesseract)
* **Precision:** 92%
* **Recall:** 87%
* **F1-Score:** 89%
* **Processing Time:** ~0.8–1.5 seconds per image (CPU)

Replacing Tesseract with deep learning-based OCR (e.g., CRNN) improved accuracy up to **95%**.

---

## 🛠️ Tech Stack

* Python
* OpenCV
* NumPy
* Tesseract OCR
* TensorFlow / Keras (CNN)

---

## 🚀 Future Improvements

* YOLO-based real-time license plate detection
* CRNN / Transformer-based OCR
* GPU acceleration & TensorRT optimization
* Deep learning-based segmentation (U-Net / Mask R-CNN)
