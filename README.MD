# 🧠 Automated Retinal Imaging for Early Diagnosis of Diabetes, Cardiac, and Ocular Diseases using CNN-LSTM

This project presents an AI-powered medical imaging system that automates early diagnosis of diabetic retinopathy, heart, and eye conditions using retinal fundus images. It uses a **hybrid CNN-LSTM architecture** to classify disease severity and generate **natural language diagnostic captions**.

---

## 🔍 Key Features

- 🧬 **DenseNet121 CNN** for retinal image feature extraction  
- 🗣️ **LSTM + GloVe embeddings** for generating readable medical captions  
- 📊 **BLEU Score Evaluation** for assessing the quality of generated text  
- 🧪 **APTOS 2019 Kaggle Dataset** used for training and evaluation  
- 🧠 Achieves up to **90% accuracy** in disease detection  
- 🌐 **Flask-based web interface** for user-friendly access  
- 🤖 **Gemini-powered chatbot** for real-time assistance

---

## 🏗️ Architecture Overview

Fundus Image ➝ DenseNet121 ➝ Feature Vectors ➝ LSTM ➝ Medical Caption
↓
Classifier ➝ Severity Level


---

## 📁 Project Structure

├── app.py # Flask server
├── main.py / # Every aspect of backend
├── index.html # Frontend interface
├── static/ # CSS, JS, images
└── README.md # This file


---

## 🧪 Dataset

- **Source**: [APTOS 2019 Blindness Detection (Kaggle)](https://www.kaggle.com/competitions/aptos2019-blindness-detection)
- **Format**: 224x224 RGB retinal images
- **Classes**:
  - 0 - No DR  
  - 1 - Mild  
  - 2 - Moderate  
  - 3-  Severe  
  - 4 - Proliferate DR

---

## 🚀 How to Run Locally

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/retinal-disease-diagnosis.git
   cd retinal-disease-diagnosis





🙏 Acknowledgements
Special thanks to the G-AIM Labs and Department of AI & ML at GRIET for infrastructure and support.
