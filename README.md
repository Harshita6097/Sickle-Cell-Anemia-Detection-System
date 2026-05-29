# 🩸 SCAResNet

### Lightweight Deep Learning Framework for Rapid Sickle Cell Detection

![Python](https://img.shields.io/badge/Python-3.10-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-DeepLearning-red)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Keras-orange)
![Streamlit](https://img.shields.io/badge/Frontend-Streamlit-green)
![Research](https://img.shields.io/badge/Research-Published-success)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

---

## 📌 Overview

SCAResNet is a lightweight deep learning framework developed for automated **Sickle Cell Anemia (SCA)** detection using microscopic blood smear images.

The project introduces a custom residual CNN architecture optimized for:

* high diagnostic accuracy,
* low computational cost,
* rapid inference,
* and deployment in resource-constrained healthcare environments.

Unlike heavy generic CNNs, SCAResNet is specifically engineered for **red blood cell morphology analysis**, enabling efficient detection of sickle-shaped cells while maintaining a compact model size.

---

## 🚀 Key Highlights

✅ Custom lightweight residual CNN architecture
✅ Automated healthy vs sickle RBC classification
✅ Real-time inference support
✅ Focal Loss optimization for hard sample learning
✅ Grad-CAM based explainability
✅ Lightweight deployment-ready model
✅ Faster inference than ResNet50 & MobileNetV2
✅ Designed for rural and low-resource healthcare environments

---

## 🧠 Model Pipeline

```text
Blood Smear Image
       │
       ▼
Preprocessing & Augmentation
       │
       ▼
SCAResNet Feature Extraction
       │
       ▼
Residual Learning Blocks
       │
       ▼
Adaptive Average Pooling
       │
       ▼
Classification Head
       │
       ▼
Healthy / Sickle Prediction
```

---

# 🏗️ SCAResNet Architecture

The proposed model introduces a custom residual block named:

## 🔬 SickleCellResBlock

Each block contains:

* Two 3×3 convolutional layers
* Batch normalization
* ReLU activation
* Identity shortcut connection

Residual Mapping:

```math
y = F(x, W_i) + x
```

The architecture is optimized for:

* RBC edge detection
* Crescent morphology extraction
* Reduced parameter count
* Fast inference

---

# 📂 Project Structure

```text
SCAResNet/
│
├── Phase-I/
│   ├── Anemia Model Phase-I.ipynb
│   └── MobileNetV2 Baseline
│
├── Phase-II/
│   ├── Anemia Model Phase-II.ipynb
│   ├── SCAResNet Architecture
│   └── Training & Evaluation
│
├── Dataset/
├── Models/
├── Results/
├── WebApp/
└── README.md
```

---

# 📊 Dataset

## Dataset Used

**aneRBC Dataset**

### Dataset Distribution

| Class       | Images |
| ----------- | ------ |
| Healthy RBC | 6000   |
| Sickle RBC  | 6000   |
| Total       | 12000  |

### Preprocessing

* Resize → `224×224`
* Z-score normalization
* RGB standardization
* Data augmentation using Albumentations

---

# ⚙️ Training Configuration

| Parameter      | Value                |
| -------------- | -------------------- |
| Framework      | PyTorch / TensorFlow |
| Optimizer      | Adam                 |
| Loss Function  | Focal Loss           |
| Batch Size     | 32                   |
| Initial LR     | 1e-3                 |
| Fine-Tuning LR | 1e-4                 |
| GPU            | NVIDIA Tesla T4      |

---

# 📈 Performance Metrics

## ✅ SCAResNet Results

| Metric    | Score  |
| --------- | ------ |
| Accuracy  | 90.42% |
| Precision | 0.93   |
| Recall    | 0.87   |
| F1-Score  | 0.90   |
| ROC-AUC   | 0.9748 |

---

# ⚡ Model Efficiency

| Model       | Accuracy         | Inference Time | Model Size |
| ----------- | ---------------- | -------------- | ---------- |
| SCAResNet   | 90.42%           | 7.6 ms         | 11.8 MB    |
| MobileNetV2 | 81.71%           | 11.3 ms        | 14.2 MB    |
| ResNet50    | Lower Efficiency | 24.5 ms        | 98 MB      |

---

# 🧪 Explainable AI (Grad-CAM)

Grad-CAM visualization confirmed that the model focuses primarily on:

* crescent-shaped RBC curvature,
* elongated cell morphology,
* and sickle-specific structural abnormalities.

This improves interpretability and trust in clinical AI-assisted diagnosis.

---

# 🌐 Web Application

The project includes a lightweight web-based diagnostic interface with:

* Blood smear image upload
* Real-time prediction
* Confidence score visualization
* Lightweight deployment support

---

# 🛠️ Installation

## Clone Repository

```bash
git clone https://github.com/yourusername/SCAResNet.git
cd SCAResNet
```

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

# ▶️ Running the Project

## Phase I

```bash
jupyter notebook "Anemia Model Phase-I.ipynb"
```

## Phase II

```bash
jupyter notebook "Anemia Model Phase-II.ipynb"
```

## Run Web Application

```bash
streamlit run app.py
```

---

# 📚 Technologies Used

* Python
* PyTorch
* TensorFlow / Keras
* OpenCV
* Albumentations
* NumPy
* Pandas
* Scikit-learn
* Streamlit
* Matplotlib

---

# 🌍 Real-World Impact

SCAResNet is designed for:

* rural healthcare centers,
* portable diagnostic systems,
* low-resource clinical environments,
* and AI-assisted hematological screening.

The lightweight architecture makes it suitable for edge-device deployment where high-end GPU resources are unavailable.

---

# 🔮 Future Scope

* Multi-class anemia classification
* Whole-slide blood smear analysis
* Edge AI optimization
* Quantization & pruning
* Mobile deployment
* Clinical multi-center validation

---

# 📖 Research Contribution

This work demonstrates that:

> Lightweight domain-specific CNN architectures can outperform heavier generalized models for medical image classification while maintaining computational efficiency.

---

# ⚠️ Disclaimer

This project is intended for research and educational purposes only and should not replace professional medical diagnosis.

---

# 👩‍💻 Author

## Harshita Sharma

B.Tech Computer Science Engineering
VIT Bhopal University

### Areas of Interest

* Deep Learning
* Medical Image Analysis
* Computer Vision
* Healthcare AI

📧 [harshita6097@gmail.com](mailto:harshita6097@gmail.com)

---

# ⭐ Acknowledgment

Special thanks to:

* aneRBC Dataset Contributors
* Open-source AI research community
* PyTorch & TensorFlow ecosystems

---

# ⭐ Support

If you found this project useful, consider starring the repository.
