# Smart Agriculture System: Tomato Leaf Disease Detection

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange)
![Deep Learning](https://img.shields.io/badge/Field-Computer%20Vision-green)

An AI-powered agricultural diagnostic tool designed to detect and classify **10 distinct types of tomato leaf diseases** with **96.3% accuracy**. This project leverages deep learning techniques, including custom **Convolutional Neural Networks (CNNs)** and **Transfer Learning (ResNet50)**, to provide a scalable solution for early disease detection and crop protection.

---

## Features

- **High Accuracy:** Achieved **96.3% test accuracy** on the PlantVillage dataset.
- **Dual Architecture:** - **Custom CNN:** Optimized for efficiency and low resource consumption.
  - **ResNet50 (Transfer Learning):** Fine-tuned for high-fidelity feature extraction.
- **Robust Preprocessing:** Implements advanced data augmentation (shear, zoom, flip) to prevent overfitting.
- **Comprehensive Evaluation:** Detailed performance metrics including Confusion Matrix, ROC-AUC Curves, Precision, Recall, and F1-Score.
- **Visualization:** Real-time plotting of training accuracy/loss and prediction confidence.

---

## Tech Stack

- **Core:** Python 3.8+
- **Deep Learning:** TensorFlow, Keras
- **Computer Vision:** OpenCV (cv2)
- **Data Manipulation:** NumPy, Pandas
- **Visualization:** Matplotlib, Seaborn
- **Model Evaluation:** Scikit-learn

---

## Dataset

The model is trained on the **PlantVillage Dataset**, specifically the Tomato Leaf subset.
- **Total Images:** ~16,000
- **Classes:** 10 (9 Disease classes + 1 Healthy class)
  1. Bacterial Spot
  2. Early Blight
  3. Late Blight
  4. Leaf Mold
  5. Septoria Leaf Spot
  6. Spider Mites (Two-spotted spider mite)
  7. Target Spot
  8. Yellow Leaf Curl Virus
  9. Mosaic Virus
  10. Healthy

---

## Model Architecture

### 1. Custom CNN
Designed from scratch with the following structure:
- **Input Layer:** (256, 256, 3) image input.
- **Convolutional Layers:** 6 layers with ReLU activation and increasing filter sizes (32 to 128).
- **Pooling Layers:** Max Pooling (2x2) for dimensionality reduction.
- **Fully Connected Layers:** Dense layers with Dropout (0.5) for regularization.
- **Output Layer:** Softmax activation for multi-class classification.

### 2. ResNet50 (Transfer Learning)
- **Pre-trained Weights:** ImageNet.
- **Fine-tuning:** Top layers frozen; custom classification head added.
- **Global Average Pooling:** Applied to reduce parameters.

---

## Results

| Metric | Score |
| :--- | :--- |
| **Test Accuracy** | **96.3%** |
| **Precision** | 0.96 |
| **Recall** | 0.95 |
| **F1-Score** | 0.95 |

*(Visualizations of the Confusion Matrix and ROC Curves can be found in the `notebooks/` directory or the project report.)*

---

## Installation & Usage

### Prerequisites
Ensure you have Python installed. It is recommended to use a virtual environment.

```bash
# Clone the repository
https://github.com/Viraj-Mavani/smart_agriculture_system.git
cd smart_agriculture_system

# Install dependencies
pip install -r requirements.txt
```

### Running the Notebook
The core logic is contained within the Jupyter Notebook for interactive exploration.

```bash
jupyter notebook "Tomato Leaf Disease Detection main.ipynb"
```

---

## Project Structure
```
.
├── Tomato Leaf Disease Detection main.ipynb   # Main training & evaluation notebook
├── Tomato Leaf Disease Detection Final Report.pdf # Detailed project report
├── requirements.txt                           # Python dependencies
├── README.md                                  # Project documentation
└── data/                                      # Dataset directory (not included in repo)

```

