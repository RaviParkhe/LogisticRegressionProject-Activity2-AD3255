# 🫀 Cardiovascular Heart Disease Prediction using Logistic Regression

An end-to-end clinical machine learning project demonstrating **Logistic Regression** for binary classification, odds ratio interpretation, and emergency risk stratification.

**Author & Developer:** [Ravi Parkhe](https://github.com/RaviParkhe)  
**Guidance & Mentorship:** [complexiota](https://github.com/complexiota)

---

## 🎯 Project Overview
- **Real-World Problem**: Cardiovascular disease is the leading cause of death globally. Rapid, interpretable risk scoring in emergency and clinical outpatient settings is critical to saving lives.
- **Why Logistic Regression?**: In healthcare and cardiology, black-box deep learning is often unusable because clinicians need **interpretable Odds Ratios ($e^{\beta}$)** to understand how specific biomarkers (e.g. ST depression, exercise-induced angina, fasting blood sugar) change the odds of heart disease.
- **Dataset**: `fedesoriano/heart-failure-prediction` from Kaggle (918 patient records across 5 clinical centers: Cleveland, Hungarian, Switzerland, Long Beach VA, Statlog).

---

## 📊 Key Results

| Metric | Result | Clinical Significance |
|---|---|---|
| **Accuracy** | **89.67%** | Nearly 9 out of 10 patients correctly diagnosed |
| **Sensitivity / Recall** | **91.18%** | Only ~8.8% false negatives at baseline |
| **Specificity** | **87.80%** | Reliable ruling out of healthy patients |
| **Precision** | **90.29%** | Positive predictions are highly trustworthy |
| **F1-Score** | **0.9073** | Strong harmonic balance between precision & recall |
| **ROC-AUC Score** | **0.9313** | Outstanding diagnostic discrimination power |
| **Cross-Entropy Loss** | **0.3323** | Calibrated posterior probabilities |

---

## 🧬 Clinical Odds Ratios ($e^{\beta}$)
- **Male Biological Sex ($OR = 1.76$)**: 76% higher odds of heart disease compared to females in this demographic cohort.
- **Fasting Blood Sugar > 120 mg/dL ($OR = 1.71$)**: High blood glucose increases odds of coronary disease by 1.71x.
- **Flat ST Slope ($OR = 1.56$)**: Significant indicator of cardiac ischemia.
- **Upward ST Slope ($OR = 0.47$)**: Strong protective factor, reducing disease odds by more than half.

---

## 🚨 Emergency Threshold Tuning
In emergency room triage, **False Negatives (missing a heart disease patient) can be fatal**. By tuning the decision threshold $\tau$:
- At **$\tau = 0.35$**, sensitivity increases to **94.12%** and missed heart attacks drop from 9 down to 6.

---

## 🔬 Assumption Testing
1. **Binary Target**: Verified (HeartDisease $\in \{0, 1\}$).
2. **Independence of Observations**: Verified (single record per patient).
3. **No Severe Multicollinearity**: Max VIF is 5.50 (well below threshold of 10).
4. **Linearity of Continuous Predictors with Log-Odds**: Box-Tidwell test confirmed stability ($r \approx 1.0$).
5. **Sample Size Adequacy**: Events-Per-Variable (EPV) = 25.4 (standard guideline recommends $> 10$).

---

## 📁 Project Structure
```text
LogisticRegressionProject/
├── Logistic_Regression_Model.ipynb   # Complete 16-step interactive Jupyter Notebook
├── README.md                         # Project documentation
└── output/                           # 9 high-resolution diagnostic plots
    ├── 01_target_distribution.png
    ├── 02_correlation_heatmap.png
    ├── 03_categorical_risk_factors.png
    ├── 04_biomarker_boxplots.png
    ├── 05_confusion_matrix.png
    ├── 06_roc_curve.png
    ├── 07_precision_recall_curve.png
    ├── 08_odds_ratios_forest_plot.png
    └── 09_probability_separation.png
```

---

## 👨‍💻 Author & Developer
- **Author**: [Ravi Parkhe](https://github.com/RaviParkhe)
- **Role**: Concept, Data Analysis, Model Building, and Implementation

---

## 🙏 Acknowledgments & Guidance
- Sincere thanks and appreciation to [@complexiota](https://github.com/complexiota) for invaluable guidance, mentorship, and support throughout the design and building of this project.
