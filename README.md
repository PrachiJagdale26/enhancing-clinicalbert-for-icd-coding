# Enhancing ClinicalBERT for ICD Coding

## Overview

This research project investigates whether contextual enhancements such as negation-aware preprocessing and section-aware preprocessing improve the performance of ClinicalBERT for automated ICD code prediction from clinical notes.

The project compares three approaches:

1. Baseline ClinicalBERT
2. Negation-Aware ClinicalBERT
3. Section-Aware ClinicalBERT

The experiments were conducted using clinical discharge summaries and multi-label ICD coding.

---

# Research Objective

ClinicalBERT is widely used for clinical NLP tasks, but it is unclear whether it explicitly benefits from:

- Negation-aware contextual preprocessing
- Clinical section-aware preprocessing

This work evaluates whether such contextual enhancements improve ICD coding performance.

---

# Models Evaluated

## 1. Baseline ClinicalBERT
Standard ClinicalBERT fine-tuned directly on discharge summaries.

## 2. Negation-Aware ClinicalBERT
Clinical notes were preprocessed using negation-aware tagging to explicitly mark negated diseases and findings.

Example:
- "No diabetes"
- "Denies chest pain"

## 3. Section-Aware ClinicalBERT
Clinical notes were reorganized using clinically important sections such as:
- History of Present Illness
- Medications
- Diagnosis
- Hospital Course

---

# Dataset

This work uses the MIMIC clinical dataset.

Due to data usage restrictions and privacy regulations, the dataset is not included in this repository.

Users must obtain access independently from PhysioNet:
https://physionet.org/content/mimiciii/

---

# Methodology

The workflow includes:

1. Clinical note preprocessing
2. Multi-label ICD code generation
3. ClinicalBERT fine-tuning
4. Evaluation using:
   - Micro Precision
   - Micro Recall
   - Micro F1
   - Macro Precision
   - Macro Recall
   - Macro F1
   - Hamming Loss

---

# Results Summary

| Model | Micro F1 | Macro F1 |
|------|------|------|
| Baseline | 30.32 | 9.66 |
| Negation-Aware | 29.03 | 9.05 |
| Section-Aware | 21.32 | 5.95 |

---

# Key Findings

- Baseline ClinicalBERT achieved the best overall performance.
- Negation-aware preprocessing slightly increased precision but reduced recall.
- Section-aware preprocessing significantly reduced performance.
- Explicit contextual preprocessing did not improve ClinicalBERT performance for ICD coding in this experimental setup.

---

# Visualizations Included

The notebook generates:

- Micro vs Macro F1 comparison
- Precision vs Recall comparison
- Performance heatmap
- ICD label distribution
- Validation loss comparison
- Confusion matrix
- Prediction error analysis

All figures are automatically saved during notebook execution.

---

# Repository Structure

clinical-icd-coding-bert/

├── Final_ClinicalBERT_ICD_Research_Notebook.ipynb
├── final_model_comparison.csv
├── requirements.txt
├── README.md
└── figures/

---

# How to Run

1. Install dependencies:

pip install -r requirements.txt

2. Open the notebook:

Final_ClinicalBERT_ICD_Research_Notebook.ipynb

3. Run all cells.

---

# Technologies Used

- Python
- PyTorch
- HuggingFace Transformers
- ClinicalBERT
- Scikit-learn
- Pandas
- NumPy
- Matplotlib
- Seaborn

---

# Research Contribution

This work provides an empirical analysis of whether explicit contextual enhancements improve ClinicalBERT for automated ICD coding.

The study contributes:
- Comparative contextual preprocessing analysis
- Multi-model evaluation
- Error analysis
- Qualitative prediction analysis

---

# Author

Research project developed for IEEE-style clinical NLP research experimentation.

# Improvements
•	better formatting
•	references
•	methodology explanation
•	results explanation
•	badges
•	installation guide
•	citations
•	figure descriptions
