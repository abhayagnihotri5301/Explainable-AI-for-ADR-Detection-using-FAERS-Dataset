Predicting Adverse Drug Reactions with Explainable AI

This document explains the project in simple terms 

---

## 🤔 What is an Adverse Drug Reaction (ADR)?

An **ADR** is an unwanted or harmful effect experienced after taking a medication.  
Some ADRs are mild (like a headache), while others can be **serious** (hospitalization, disability, or death).

Governments collect reports of ADRs to monitor drug safety. One such system is **FAERS** – the FDA Adverse Event Reporting System.

---

## 🎯 What Was the Goal of This Project?

The main goals were:

1. Use real-world FAERS data to **predict** if an ADR is serious or not.
2. Use **Explainable AI (XAI)** to show why the model made each prediction.
3. Build a transparent and useful machine learning tool that supports safer drug use.

---

## 🔬 What is Explainable AI (XAI)?

Machine learning models are often seen as "black boxes" – they give results, but we don’t know why.

**XAI** (e.g. SHAP) helps explain:
- Which features influenced the prediction
- How much each factor contributed

This builds trust — especially in sensitive fields like healthcare.

---

## 🧪 What Data Did We Use?

We used 3 parts of the FAERS dataset (Q4 2024):
- `DEMO`: Patient info (age, gender, weight)
- `DRUG`: Drug info (name, role)
- `REAC`: Reactions (e.g., vomiting, rash)

We merged these on a unique report ID (`primaryid`), and created a new column:
- `serious` = 1 if the outcome was serious (death, hospitalization, etc.)

---

## 🧠 How Did the Model Work?

1. We trained an **XGBoost** model (a decision tree algorithm) to classify if an ADR was serious.
2. Input features included age, gender, role of drug (primary suspect or not), etc.
3. The model learned patterns from thousands of reports.

---

## 📈 What Did the Explainability Show?

Using SHAP (SHapley Additive exPlanations), we saw:
- Age and gender were major influencers
- "Primary suspect" drugs were more likely to cause serious ADRs
- Certain drug indications and routes had patterns

This makes the model **transparent and interpretable** — a key requirement in medical applications.

---

## 💡 Why Is This Important?

- ADRs are a major public health issue.
- Predictive models can help identify high-risk patients earlier.
- SHAP provides accountability and trust in AI decisions.
- This project is a small but real step toward safer and smarter healthcare using data science.

---

## 🇯🇵 Why This Project for MEXT Japan?

Japan values innovation in **AI and life sciences**. This project shows how I:
- Integrated my **pharmaceutical background** with data science
- Used open government health data (FAERS)
- Focus on **real-world impact** using explainable AI

It aligns with Japan’s vision of safe and ethical AI in healthcare.

---

## 📬 About Me

**Abhay Agnihotri**  
Bachelor's in Pharmacy (India)  
Learning data analytics and AI  
Passionate about healthcare innovation

