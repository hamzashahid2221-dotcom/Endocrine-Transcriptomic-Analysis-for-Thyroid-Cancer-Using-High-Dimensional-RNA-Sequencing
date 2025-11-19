# Endocrine Transcriptomic Analysis for Thyroid Cancer Using High-Dimensional RNA Sequencing

This repository presents an **explainable machine learning framework** for thyroid cancer detection using **20,530-gene RNA sequencing data**.  
The project focuses on:

- **Endocrine-specific gene expression patterns**  
- **Robust detection despite limited non-cancer samples**  
- **Functionally relevant transcriptomic biomarker identification**

The goal is to combine high diagnostic accuracy with **biologically interpretable insights** relevant to thyroid cancer pathology.

---

## 📌 Dataset Overview

- **Number of features:** 20,530 genes  
- **Target Variable:** `sample_type_id`  
  - `0.0` → Non-cancer thyroid tissue  
  - `1.0` → Cancerous thyroid tissue  
- **Challenge:** High-dimensional dataset with limited non-cancer samples  
- **Objective:** Identify key endocrine-related gene signatures while maintaining robust classification performance

---

## 🔍 Project Novelty

### ⭐ 1. Endocrine-Specific Transcriptomic Insights  
Unlike generic cancer detection, this project emphasizes genes related to thyroid hormone regulation, endocrine signaling, and tissue-specific pathways.

### 🧬 2. Rare Sample Sensitivity  
Non-cancer samples are limited. The workflow addresses this through careful feature selection and robust model validation, achieving high recall for the minority class.

### 🧠 3. Functional Biomarker Interpretation  
Top-ranked genes (e.g., **GABRB2, SRCIN1, IGSF10**) provide insights into endocrine signaling disruptions and potential thyroid cancer mechanisms.

---

## ⚙️ Methodology Overview

1. **Data Preprocessing**  
   - Normalization of RNA-seq expression values  
   - Handling of 20,530 high-dimensional features

2. **Feature Selection**  
   - Mutual Information to extract thyroid-relevant genes  

3. **Classification**  
   - XGBoost optimized for imbalanced, high-dimensional datasets  

4. **Evaluation**  
   - Classification metrics  
   - 5-fold cross-validation for stability  
   - Explainable gene-level insights  

---

## 📈 Model Performance

### **Classification Report**

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| 0.0 (Non-Cancer) | 1.00 | 0.82 | 0.90 | 17 |
| 1.0 (Cancer)     | 0.98 | 1.00 | 0.99 | 155 |

- **Accuracy:** 0.98  
- **Macro F1 Score:** 0.95  
- **Weighted F1 Score:** 0.98  

> Demonstrates strong diagnostic performance, even with limited non-cancer samples.

---

## 🔁 Cross-Validation Performance (5-Fold)

| Fold | Accuracy |
|------|----------|
| 1 | 1.000 |
| 2 | 0.9875 |
| 3 | 0.9875 |
| 4 | 0.9625 |
| 5 | 0.9875 |

**Average Accuracy:** 0.985  

> Consistent fold performance shows the model’s robustness.

---

## 🧬 Top Thyroid-Related Genes Identified (Feature Importance)

| Rank | Gene | Importance |
|------|-------|------------|
| 1 | **GABRB2** | 0.12739 |
| 2 | **SRCIN1** | 0.08506 |
| 3 | IGSF10 | 0.06406 |
| 4 | ABCA9 | 0.05894 |
| 5 | AGPAT4 | 0.04341 |
| 6 | SEMA3C | 0.04244 |
| 7 | MLF1 | 0.04064 |
| 8 | TUBG1 | 0.03226 |
| 9 | FAM84A | 0.03042 |
| 10 | DPT | 0.02659 |
| 11 | TFF3 | 0.02608 |
| 12 | FGF14 | 0.02607 |
| 13 | ORMDL3 | 0.02418 |
| 14 | EYA1 | 0.02238 |
| 15 | STAB2 | 0.02127 |
| 16 | SLC6A15 | 0.01404 |
| 17 | TCEAL7 | 0.01372 |
| 18 | CDH13 | 0.01347 |
| 19 | ENTPD1 | 0.01218 |
| 20 | ACSM2B | 0.01181 |

### 🧠 Biological Interpretation
- **GABRB2** and **SRCIN1** are linked to endocrine signaling and thyroid-specific transcription.  
- Several other genes highlight thyroid hormone regulation and cell adhesion pathways.  
- Provides a starting point for **functional validation and clinical research**.

---

## 🧠 Key Takeaways

- High diagnostic accuracy (**98%**) with **rare-class sensitivity**.  
- Explains **thyroid-specific transcriptomic alterations** using feature importance.  
- Robust across **cross-validation folds**, demonstrating reproducibility.  
- Useful for **biomarker discovery and endocrine cancer research**.

---

## 🛠 Tools Used

- Python  
- XGBoost  
- Scikit-Learn  
- NumPy & Pandas  
- Matplotlib / Seaborn (optional for visualization)

---

## 🤝 Contribution

This repository is for **methodology demonstration and reproducible research**.  
For questions, collaborations, or discussions, feel free to open an issue.
