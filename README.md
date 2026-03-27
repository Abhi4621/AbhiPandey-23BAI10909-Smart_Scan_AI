# VisionScan: Integrated Document Processing & Classification Pipeline

## 📝 Project Overview
**VisionScan** is a comprehensive Computer Vision application developed for the **Bring Your Own Project (BYOP)** component at VIT Bhopal. The system automates the transition from a raw, angled photograph of a document to a rectified, high-contrast digital scan. 

Beyond simple scanning, the pipeline utilizes mathematical morphology and geometric transformations to classify the document type (e.g., ID Card vs. A4 Page) and assess scan quality.

---

## 🎓 Syllabus Mapping (Course Concepts Applied)
This project demonstrates the practical application of all 5 modules from the Computer Vision course:

| Module | Course Concept | Implementation in Project |
| :--- | :--- | :--- |
| **Module 1** | Image Formation & Representation | Perspective Transformation ($3 \times 3$ Matrix) and Resizing. |
| **Module 2** | Image Enhancement | Bilateral Filtering for noise reduction and Morphological Closing/Erosion. |
| **Module 3** | Feature & Edge Detection | Canny Edge Detection and Contour Approximation (`approxPolyDP`). |
| **Module 4** | Image Segmentation | Adaptive Gaussian Thresholding and Otsu’s Binarization. |
| **Module 5** | Object Classification | Logic-based classification using Aspect Ratio and Histogram Std Dev. |

---

## 🚀 Getting Started

### 1. Prerequisites
Ensure you have **Python 3.8+** installed. It is recommended to use a virtual environment.

### 2. Installation
Clone the repository and install the required dependencies:
```bash
git clone [https://github.com/YOUR_USERNAME/YOUR_REPO_NAME](https://github.com/YOUR_USERNAME/YOUR_REPO_NAME)
cd YOUR_REPO_NAME
pip install -r requirements.txt
3. Usage (Command Line execution)
Run the scanner by providing the path to an image file:
python scanner.py --image path/to/your/document.jpg
🛠️ Technical Pipeline
Noise Reduction: Uses a Bilateral Filter to smooth textures while preserving document edges.

Edge Detection: Applies the Canny algorithm to identify the high-gradient boundaries of the paper.

Contour Analysis: Searches for the largest 4-sided polygon to locate the document corners.

Perspective Warp: Maps the 4 corners to a new top-down view, correcting camera tilt.

Binarization: Converts the warped image to black-and-white using Otsu’s method for maximum text readability.

Classification: Analyzes the resulting image dimensions to categorize the document type.

📊 Evaluation Parameters
Fully Executable: Supports CLI arguments via argparse.

Engineering Practices: Modular code structure with clear function definitions.

Accuracy: Robust against varied lighting and background textures.
