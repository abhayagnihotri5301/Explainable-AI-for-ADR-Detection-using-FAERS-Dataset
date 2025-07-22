
# FAERS Adverse Drug Reaction (ADR) Prediction with Explainable AI (SHAP)

This project uses the publicly available FAERS (FDA Adverse Event Reporting System) dataset to predict the likelihood of serious adverse drug reactions (ADRs) and explains the model decisions using SHAP (SHapley Additive exPlanations). The aim is to combine real-world pharmacovigilance data with interpretable machine learning to support drug safety research.

---

## 🔍 Problem Statement

Can we use patient demographic and drug-related information from the FAERS database to predict the seriousness of reported adverse drug reactions?  
How can we **explain** these predictions to improve trust and usability in a healthcare setting?

---

## 📦 Dataset

- Source: [FAERS Q4 2024](https://fis.fda.gov/extensions/FPD-QDE-FAERS/FPD-QDE-FAERS.html)
- Merged tables: `DEMO24Q4`, `DRUG24Q4`, `REAC24Q4`
- Final dataset size: 21 million+ rows, downsampled for modeling
- Label: `serious` (binary: 1 = serious outcome, 0 = non-serious)

---

## 🧠 Tools & Technologies

- **Python 3.11**
- **pandas**, **numpy** – data cleaning and transformation
- **xgboost** – machine learning classification model
- **shap** – explainable AI for feature impact analysis
- **matplotlib**, **seaborn** – data visualization

---

## 🧪 Methodology

1. **Data Cleaning & Merging**
   - Cleaned and merged FAERS data on `primaryid`
   - Engineered `serious` flag from outcome columns

2. **Model Training**
   - Trained an `XGBoostClassifier` to predict ADR seriousness
   - Evaluated with classification metrics

3. **Explainability**
   - Applied SHAP to identify most influential features
   - Visualized feature contributions using SHAP summary plots

---

## 📊 Results (Example)

- Key features influencing predictions:
  - Age
  - Role code (primary suspect/concomitant)
  - Gender
  - Drug route and indication

![SHAP summary plot placeholder](shap_plot.png)

---

## 🧑‍💻 How to Run

1. Clone this repo
2. Install required packages:
   ```bash
   pip install pandas xgboost shap matplotlib
   ```
3. Run `faers_setup.ipynb` in Jupyter or VS Code
4. Explore SHAP values at the end of the notebook

---

## 📁 File Structure

```
/FAERS_ADR_XAI/
├── faers_setup.ipynb           # Main notebook
├── data/                       # Merged CSV files (not included)
├── README.md                   # Project overview
├── EXPLAIN.md                  # Beginner-friendly explanation
└── shap_plot.png               # SHAP summary plot (optional)
```

---

## 📚 Inspiration

This project was built to demonstrate how data science and explainable AI can support pharmacovigilance, with the potential to assist regulators, researchers, and clinicians in making safer decisions.

---

## 📬 Contact

Abhay Agnihotri  
📧 abhayagnihoti536@gmail.com  
📍 India  
🧪 Background: BPharm + Data Analytics

---

