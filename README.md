# 📌 BSDS500 Dataset for Hybrid Marker Extraction Method by Gradient and Spectral Features for Marker-Controlled Watershed Segmentation (HMEGS) Research

[![License](https://img.shields.io/badge/License-CC%20BY%204.0-green)](https://creativecommons.org/licenses/by/4.0/)
[![Dataset](https://img.shields.io/badge/Dataset-BSDS500-blue)](https://www2.eecs.berkeley.edu/Research/Projects/CS/vision/grouping/resources.html)

This repository provides the **BSDS500 dataset**, a benchmark dataset for **image segmentation and edge detection**. It contains manually labeled **ground-truth segmentations** and is used in our research on **Hybrid Marker Extraction by Gradient and Spectral Features (HMEGS)** for **marker-controlled watershed segmentation**.

## 📄 Research Paper
This dataset supports our research paper:

**📌 Title:** *A Hybrid Marker Extraction Method by Gradient and Spectral Features for Marker-Controlled Watershed Segmentation*  
**✍️ Authors:** S.B. Hossaini, S.M. Mousavi, A. Bavafatoosi  
**📕 Submitted to:** *### (Springer)*  
**🔗 Related Code Repository:** [HMEGS Implementation](https://github.com/sbehzadh9/HMEGS)

## 📂 Dataset Structure
The **BSDS500 dataset** consists of **500 natural images**, each with multiple **manually annotated segmentations**. The dataset is divided as follows:

```
BSDS500/
│── images/           # Contains raw images
│   ├── train/       # 200 training images
│   ├── val/         # 100 validation images
│   ├── test/        # 200 test images
│
│── groundTruth/      # Hand-labeled segmentations (MAT files)
│   ├── train/       # Corresponding ground truth for train images
│   ├── val/         # Corresponding ground truth for val images
│   ├── test/        # Corresponding ground truth for test images
│
│── human/            # Multiple human annotations per image
│── README.md         # Dataset documentation
```

## 📥 Download Dataset
The original dataset is available from the **Berkeley Vision Group**:  
🔗 [Official BSDS500 Dataset](https://www2.eecs.berkeley.edu/Research/Projects/CS/vision/grouping/resources.html)

Alternatively, you can clone this repository:

```bash
git clone https://github.com/your-repo/BSDS500-Segmentation-Dataset.git
```
## 🚀 Usage
To use the dataset for segmentation experiments, you can load the images and ground-truth segmentations in **Python**:

```python
import scipy.io as sio
import cv2
import numpy as np

# Load an example ground-truth segmentation
gt_data = sio.loadmat('BSDS500/groundTruth/181091.mat')
image = cv2.imread('BSDS500/images/test/181091.jpg')

# Display the original image
cv2.imshow('Image', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## 📜 License
This dataset follows the **Creative Commons Attribution 4.0 International (CC BY 4.0) License**.  
📄 For more details, see the **[LICENSE](https://creativecommons.org/licenses/by/4.0/)** file.

