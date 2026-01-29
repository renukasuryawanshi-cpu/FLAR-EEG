# FLAR-EEG
Feature-Level Age Regression for EEG Spectral Deconfounding (FLAR-EEG) — a reproducible pipeline that residualizes canonical band-limited EEG power features with respect to chronological age to produce age-deconfounded representations for downstream analysis.
# FLAR-EEG  
**Feature-Level Age Regression for EEG Spectral Deconfounding**  

A reproducible Python pipeline for removing age-related variance from EEG spectral features in large-scale lifespan datasets.

---

## 📌 Overview

Age is a dominant confound in EEG spectral measures across adulthood and can obscure task-related, emotional, and clinically meaningful neural signatures. **FLAR-EEG** provides a standardized, feature-level regression framework that explicitly removes chronological age effects from EEG spectral features while preserving their underlying distributions.

This pipeline is designed for large lifespan datasets such as **Cambridge Centre for Ageing and Neuroscience (Cam-CAN)** and supports reproducible benchmarking before and after age regression.

---

## 🎯 Key Contributions

- Feature-level age regression of EEG spectral power (Delta, Theta, Alpha, Beta)
- Quantitative evaluation of:
  - Age–EEG correlation (before vs after regression)
  - Variance removed by age regression
  - Distribution preservation (mean, variance, skewness, kurtosis)
  - Effect sizes between age groups
- Fully reproducible pipeline suitable for lifespan, emotion, and cognitive EEG studies
- MethodsX-compliant methodological documentation

---

## 📊 Dataset

- **Cambridge Centre for Ageing and Neuroscience (Cam-CAN)**
- Adult lifespan EEG data (18–88+ years)
- Publicly available upon request

🔗 https://www.cam-can.org

---

## 🧠 Method Summary

1. **EEG Preprocessing**
   - Band-pass filtering
   - Artifact rejection (as provided by Cam-CAN preprocessing)

2. **Spectral Feature Extraction**
   - Band-limited power computation:
     - Delta (1–4 Hz)
     - Theta (4–8 Hz)
     - Alpha (8–13 Hz)
     - Beta (13–30 Hz)

3. **Feature-Level Age Regression**
   - Linear regression of each spectral feature against chronological age
   - Residuals retained as age-deconfounded features

4. **Validation & Benchmarking**
   - Correlation analysis (feature vs age)
   - Variance decomposition (before vs after regression)
   - Distributional statistics comparison
   - Effect size analysis between age groups

---

## 📈 Key Outputs

- **Figures**
  - EEG feature vs age (before vs after regression)
  - Age-related variance removed by regression
  - Distribution preservation check
  - Sex- and age-stratified validation (women)

- **Tables**
  - Dataset characteristics
  - EEG feature distribution statistics
  - Proportion of age-related variance removed
  - Effect size comparisons (Cohen’s d)

---

## 🛠 Software Requirements

- Python ≥ 3.9
- NumPy
- Pandas
- SciPy
- scikit-learn
- statsmodels
- MNE-Python
- Matplotlib / Seaborn

Install dependencies:
```bash
pip install -r requirements.txt

