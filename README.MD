# Retinal Disease Diagnosis with Medical Captioning

An AI system that takes retinal fundus images as input and outputs both a disease severity grade and a natural language diagnostic caption. Built as a final-year project at GRIET with support from G-AIM Labs.

---

## What it does

Given a retinal fundus image, the system:
1. Classifies diabetic retinopathy severity on the APTOS 0–4 scale (No DR → Proliferative DR)
2. Generates a short medical caption describing the findings
3. Serves both through a Flask web interface with a Gemini-powered chatbot for follow-up questions

---

## Architecture

**Classification:** DenseNet121 (pretrained, fine-tuned on APTOS 2019) extracts feature vectors from 224×224 RGB fundus images. Final layers predict one of 5 DR severity grades.

**Captioning:** Feature vectors from DenseNet121 feed into an LSTM decoder with GloVe word embeddings to generate diagnostic text. Caption quality is evaluated with BLEU score.

```
Fundus Image → DenseNet121 → Feature Vector → LSTM Decoder → Medical Caption
                                    ↓
                             FC Classifier → Severity Grade (0–4)
```

---

## Dataset

**APTOS 2019 Blindness Detection** (Kaggle)  
- 224×224 RGB retinal fundus images  
- 5 classes: No DR (0), Mild (1), Moderate (2), Severe (3), Proliferative DR (4)  
- Link: https://www.kaggle.com/competitions/aptos2019-blindness-detection

---

## Results

| Metric | Value |
|--------|-------|
| Classification accuracy | 90% |
| Caption evaluation | BLEU score |

---

## Stack

- Python, PyTorch
- DenseNet121 (torchvision), LSTM, GloVe embeddings
- Flask (web interface)
- Google Gemini API (chatbot)
- APTOS 2019 dataset

---

## Project structure

```
app.py          # Flask server and routes
main.py         # Model inference and caption generation
index.html      # Frontend
static/         # CSS, JS, assets
```

---

## Run locally

```bash
git clone https://github.com/NoahSama01/Diabetes-Heart-Disease-prediction.git
cd Diabetes-Heart-Disease-prediction
pip install -r requirements.txt
python app.py
```

---

## Acknowledgements

G-AIM Labs and the Department of AI & ML at GRIET for compute resources and guidance.
