# VisionScan: Integrated Document Processing & Classification Pipeline

**Course:** Computer Vision (BYOP)  
**Author:** Abhi Pandey (Reg No: 23BAI10909)  
**Institution:** VIT Bhopal University  

---

## 📌 Project Overview
VisionScan is an end-to-end Computer Vision pipeline designed to automate the digitization of physical documents. It addresses real-world issues like perspective distortion, noise in scanned images, and the need for automated categorization.

### Key Capabilities:
* **Document Straightening (Perspective Transform):** Automatically detects document corners and performs a 4-point perspective wrap to create a "top-down" scan view.
* **Image Enhancement:** Uses adaptive thresholding and Gaussian blurring to remove shadows and highlights for better readability.
* **OCR (Optical Character Recognition):** Extracts raw text from processed images using Tesseract/EasyOCR.
* **Classification:** Categorizes documents (e.g., Invoice, ID Card, Letter) based on extracted features and layout analysis.

---

## 🛠️ Computer Vision Pipeline
The project utilizes several core CV concepts covered in the course:

1.  **Preprocessing:** Grayscale conversion and bilateral filtering to reduce noise while preserving edges.
2.  **Edge Detection:** Implementation of the **Canny Edge Detection** algorithm to find document boundaries.
3.  **Contour Analysis:** Utilizing `cv2.findContours()` to identify the largest quadrilateral in the frame.
4.  **Geometric Transformations:** Applying a **Perspective Transform** matrix to rectify warped document images.
5.  **Thresholding:** Otsu’s Binarization for high-contrast text extraction.

---

## 🚀 Visual Results
| Input (Warped/Noisy) | Processed (Thresholded) | Final Scanned Output |
| :---: | :---: | :---: |
| ![Input](input_image.jpeg) | ![Threshold](pre_process_image.png) | ![Output](output_image.png) |


---

## 📂 Repository Structure
* `VisionScan_..._(CODE).ipynb`: The primary implementation notebook containing the pipeline logic.
* `23BAI10909_..._(Report).pdf`: Detailed technical documentation and project reflection.
* `data/`: Sample input images used for testing.

---

## ⚙️ Setup & Installation
1. Clone the repository:
   ```bash
   git clone [https://github.com/Abhi4621/AbhiPandey-223BAI10909-VisionScan-CV-Pipeline.git](https://github.com/Abhi4621/AbhiPandey-223BAI10909-VisionScan-CV-Pipeline.git)
   Install dependencies:

Bash
pip install opencv-python numpy pytesseract matplotlib
Run the notebook:
Open the .ipynb file in Jupyter or Google Colab and execute the cells sequentially.
