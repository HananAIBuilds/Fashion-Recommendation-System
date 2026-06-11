# 👗 Fashion Recommendation System

![Python](https://img.shields.io/badge/Python-3.10-blue?style=flat-square&logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Deep%20Learning-orange?style=flat-square&logo=tensorflow)
![Streamlit](https://img.shields.io/badge/Streamlit-Web%20App-red?style=flat-square&logo=streamlit)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat-square)

---

## 📌 Project Overview

A deep learning-powered fashion recommendation system trained on the **Fashion MNIST dataset (70,000 images)**. The system uses a custom CNN with Residual Blocks and Multi-Head Attention to learn visual features, then recommends visually similar fashion items using cosine similarity.

---

## 🧠 How It Works
Fashion MNIST Dataset (70,000 images)
↓
Data Augmentation (rotation, zoom, flip)
↓
Custom CNN Training
(Conv2D → Residual Block → Multi-Head Attention → Dense)
↓
Feature Extraction (128-dim embedding per image)
↓
Cosine Similarity Calculation
↓
Top-5 Similar Items Recommended
↓
Streamlit Web App

---

## 🏗️ Model Architecture

| Layer | Details |
|-------|---------|
| Conv2D + BatchNorm | 32 filters, 3×3, ReLU |
| MaxPooling | 2×2 |
| **Residual Block** | Skip connection with BatchNorm + ReLU |
| **Multi-Head Attention** | 2 heads, key_dim=32 |
| Flatten + Dense | 128 units, ReLU |
| Dropout | 0.5 |
| Output | 10 classes, Softmax |

**Why Residual + Attention?**
- Residual blocks prevent vanishing gradients in deeper networks
- Multi-Head Attention lets the model focus on important spatial regions

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 👗 Fashion Classification | 10 categories (T-shirt, Trouser, Dress, etc.) |
| 🔍 Visual Recommendation | Top-5 similar items via cosine similarity |
| 📊 Full Evaluation | Confusion matrix, classification report, loss/accuracy curves |
| 🔁 Data Augmentation | Rotation, zoom, shift, horizontal flip |
| 💾 Model Export | Saved as model.h5 for deployment |
| 🌐 Web App | Interactive Streamlit UI with image slider |

---

## 📊 Training Details

| Setting | Value |
|---------|-------|
| Dataset | Fashion MNIST |
| Train/Val Split | 80% / 20% |
| Batch Size | 32 |
| Max Epochs | 30 |
| Optimizer | Adam |
| Loss | Categorical Crossentropy |
| Early Stopping | Patience = 5 |
| LR Reduction | Factor 0.5, Patience = 3 |

---

## 🛠️ Tech Stack

| Library | Purpose |
|---------|---------|
| TensorFlow / Keras | Model training & feature extraction |
| Scikit-learn | Cosine similarity, KNN, evaluation |
| Streamlit | Web app deployment |
| NumPy | Array operations |
| Matplotlib / Seaborn | Training curves, confusion matrix |

---

## ▶️ How to Run

```bash
# 1. Clone the repo
git clone https://github.com/ChintoHacker/Fashion-Recomended-Sytsem.git
cd Fashion-Recomended-Sytsem

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run the app
streamlit run app.py
```

> **Note:** model.h5 must be present in the root directory.
> If missing, run Recomende_System.ipynb first to train and save the model.

---

## 📁 Project Structure
Fashion-Recomended-Sytsem/
├── app.py                    # Streamlit web app
├── Recomende_System.ipynb    # Training notebook
├── model.h5                  # Trained CNN model
├── requirements.txt
└── README.md

---

## 💡 Skills Demonstrated

- Custom CNN architecture design (Residual + Attention)
- Deep Learning with TensorFlow/Keras
- Data Augmentation pipeline
- Feature extraction from intermediate layers
- Cosine similarity for content-based recommendation
- Model evaluation (confusion matrix, classification report)
- Streamlit web app deployment

---

## 👤 Author

**Abdul Hanan**
BS Information Technology — KFUEIT, Rahim Yar Khan
