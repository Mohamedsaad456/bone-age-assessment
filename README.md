# bone-age-assessment

This project aims to estimate the **bone age** of children using **hand X-ray images** and compare it with their chronological age to help diagnose growth-related conditions or detect inconsistencies in reported age (e.g., in immigration or sports registration).

---

## Problem Statement

Bone age assessment is a clinical task used to evaluate the maturity of a child's skeletal system. Automating this process using deep learning can:
- Assist doctors in diagnosing growth disorders (e.g., delayed growth).
- Identify children using false ages in contexts like illegal immigration or sports clubs.

---

## Dataset & Preprocessing

We used a publicly available dataset of **hand X-ray images**.  
We applied several **image preprocessing techniques** including:
- **CLAHE (Contrast Limited Adaptive Histogram Equalization)** for enhancing contrast.

---

## Deep Learning Models Used

We experimented with multiple models and input types to find the best architecture:

### 1. Xception Model

- **Single Input**: Hand X-ray image only  
- **Multi Input**: Hand X-ray image + Gender  

🟢 **Best Results were achieved by this model (Multi-Input):**
- **MAE (Mean Absolute Error):** 8.5
- **R² Score:** 0.93

---

### 2. ResNet-50 Model

- **Single Input**: Hand X-ray image only  
- **Multi Input**: Hand X-ray image + Gender  

These models were also trained and evaluated for comparison, but the Xception-based model outperformed them.

---

## User Interface

We built an interactive demo using **Gradio** that allows users to upload a hand X-ray and specify gender to get the predicted bone age.

Try the model on Hugging Face: [Insert Hugging Face Link Here]

---

## Code Repository

All code, models, and training scripts are available in this repository.

 GitHub Repository: [Insert GitHub Link Here]

---

## Evaluation Metrics

- **MAE (Mean Absolute Error)**
- **R² Score**
- Loss curves and evaluation plots are included in the `results/` folder.

---

##  Dependencies

- Python 3.8+
- TensorFlow / Keras
- Gradio
- NumPy / Pandas / Matplotlib
- OpenCV

Install dependencies using:

```bash
pip install -r requirements.txt
