# 🧠 Detecting and Preventing AI-Generated Misinformation in Low-Information Communities using Explainable Machine Learning

## 📘 Overview
We are building simple and practical tools that detect and explain fake videos and AI-generated text that target people in low-information communities.  
Our goal is to give clear, fast, and understandable signals that a message or video may not be real and to explain **why** it was flagged.

This project is part of our AI safety work at **Ewooral & BFAM Holdings**, aimed at protecting rural and under-informed communities from misinformation, deepfakes, and manipulated media.

---

## ⚖️ Why This Matters
Many people in rural and low-information areas believe what they see or read online without questioning it.  
When false videos or AI-generated messages spread, they can harm reputations and create real-world damage.  

Our company experienced this firsthand when a **fake video** misrepresented our CEO. That incident motivated us to study **AI Safety** especially how to detect and reduce harmful AI-generated outputs.

This project links to AI safety by exploring **how models create deceptive or harmful content**, and **how we can detect and explain** such risks transparently.

---

## 🔍 Main Research Question
> How can we detect AI-generated video and text in low-resource settings and provide short, human-readable explanations for detections?

---

## 🎯 Objectives
- Develop a **deepfake video detection model** for low-resource setups.  
- Build a **text classifier** to detect AI-generated or manipulated messages.  
- Create **explainable AI tools** (XAI) that help non-experts understand model reasoning.  
- Test and validate on simulated datasets reflecting rural communication styles.  
- Produce a **short paper**, **GitHub repository**, and **demo blog post**.

---

## 📦 Datasets and Data Plan

### Public Datasets
- **FaceForensics++** – For video deepfake samples.  
- **DFDC (Deepfake Detection Challenge)** – For large-scale detection benchmarking.  
- **Celeb-DF** – For high-quality deepfake videos.  
- **Human-written & AI-generated text** – Collected from news and LLM outputs.

### Local Data Creation
- Small sample of **community-style videos and messages** using local languages and names.  
- Synthetic social posts or WhatsApp-like messages, collected ethically with consent.  
- Focus on *Ghanaian rural communication formats* for authenticity.

---

## 🔒 Ethics and Privacy
- Use only **public** or **consented** data.  
- Anonymize any human faces or identities in training data.  
- Maintain a `data_license.md` file listing sources and usage terms.  
- Follow AI ethics guidelines for misinformation research.

---

## 🧰 Methods and Tools

### Core Libraries
- `PyTorch` — Model training and fine-tuning  
- `Transformers` (Hugging Face) — For text-based detection  
- `OpenCV`, `FFmpeg` — Video and frame extraction  
- `MTCNN` or `dlib` — Face detection  
- `Librosa` — Audio feature extraction  
- `SHAP`, `LIME`, `Grad-CAM` — Model interpretability and explainability  

### Model Concepts

#### 🎞 Video Pipeline
1. Extract and preprocess frames using OpenCV  
2. Detect and crop faces per frame  
3. Train a lightweight CNN or fine-tuned pretrained backbone  
4. Combine temporal and (optionally) audio features  

#### ✍ Text Pipeline
1. Train a transformer to detect synthetic text  
2. Analyze perplexity and unusual structure patterns  
3. Highlight tokens and words that triggered flags  

---

## 🧩 Explainability
- **Video:** Use Grad-CAM visual maps to show why a frame was flagged.  
- **Text:** Use SHAP or LIME to highlight suspicious word patterns or anomalies.  

---

## 📊 Evaluation Metrics
- Precision, Recall, F1 Score  
- ROC-AUC for classification quality  
- Robustness under compression, noise, and scaling  
- Human evaluation for explanation clarity  

---

## 🗓 12-Week Project Schedule

| Weeks | Task |
|-------|------|
| Week 0 | Setup repo, prepare datasets |
| Weeks 1–2 | Data loaders, baseline text/video models |
| Weeks 3–4 | Improve models, add temporal pooling |
| Week 5 | Add explainability features |
| Week 6 | Robustness testing and fine-tuning |
| Week 7 | Small local user study for explainability |
| Weeks 8–9 | Paper draft and documentation |
| Week 10 | Code cleanup and reproducibility checks |
| Week 11 | Final experiments and reporting |
| Week 12 | Deliverables (paper, blog, demo, GitHub push) |

---

## 🧾 Deliverables
- Public GitHub repo with full source code  
- Dataset samples and data generation scripts  
- Model checkpoints and evaluation logs  
- A 2-page workshop paper draft  
- Blog post + demo notebook explaining findings  

---

## 📁 Repository Structure
```bash
bfam-misinformation-safety/
├── README.md
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
│   └── demo.ipynb
├── src/
│   ├── data.py
│   ├── model_video.py
│   ├── model_text.py
│   ├── train.py
│   ├── eval.py
│   └── explain.py
├── experiments/
│   └── logs/
├── requirements.txt
└── LICENSE



⚙️ Installation and Setup
1️⃣ Clone Repository