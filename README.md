# 🍷 Wine Quality Analysis — Capstone Project

> **Tools:** Python · Power BI · Excel  
> **Domain:** Food & Beverage / Machine Learning  
> **Type:** XDi Certified Data Analyst — Capstone Project (April 2025)  
> **Mentor:** Manuel Bordasch

---

## 🎯 Project Goal

Investigate the chemical and physical properties that influence red wine quality ratings,
and build a predictive model to forecast quality scores based on measurable features.

**Core business questions:**
- Which chemical properties have the strongest influence on wine quality?
- Can wine quality be reliably predicted from physicochemical data?
- Which ML model performs best for this regression task?

---

## 📌 Key Results

| Metric | Value |
|--------|-------|
| 🍷 Total Wine Samples | 1,143 |
| 🔬 Features Analyzed | 13 (alcohol, pH, citric acid, sulphates...) |
| 🥇 Best Model | **Random Forest** (R² = 0.462) |
| 📉 Best MSE | **0.2989** (Random Forest) |
| 🔑 Top Predictor | **Alcohol content** |

---

## 🤖 Model Comparison

| Model | R² Score | MSE |
|-------|----------|-----|
| **Random Forest** ✅ | **0.462** | **0.2989** |
| XGBoost | 0.343 | 0.3655 |
| Linear Regression | 0.317 | 0.3800 |

> ✅ **Random Forest achieved the best predictive performance** with the highest R² score
> and lowest Mean Squared Error across all three models.

---

## 🔍 Key Insights

### 1 · Alcohol is the Strongest Quality Predictor
Alcohol content showed the highest feature importance in both Random Forest and XGBoost models,
with a clear positive correlation — higher alcohol content consistently correlates with higher quality ratings.

### 2 · Volatile Acidity Negatively Impacts Quality
Volatile acidity ranked second in feature importance and showed a strong **negative** correlation
with quality. High acidity leads to unpleasant vinegar-like taste, reducing perceived quality.

### 3 · Sulphates Play a Supporting Role
Sulphates ranked third in importance, showing a moderate positive correlation with quality.
They act as a preservative and antioxidant, contributing to wine stability and taste.

### 4 · Top 3 Features (Random Forest Feature Importance)
```
1. alcohol          → 0.27 importance
2. volatile acidity → 0.15 importance  
3. sulphates        → 0.13 importance
```

### 5 · Quality Distribution is Imbalanced
Most wines score between **5 and 6** on the quality scale (0–10),
with very few extreme scores (3 or 8+), making prediction at the extremes more challenging.

> 💡 **Production Recommendation:** Focus quality control on alcohol content optimization
> and volatile acidity reduction. These two factors alone explain the majority of quality variation.

---

## 🛠️ Tools & Technologies

| Layer | Tools Used |
|-------|-----------|
| Data Cleaning & EDA | Python · Pandas · NumPy · Matplotlib · Seaborn |
| Machine Learning | Scikit-Learn · XGBoost (Random Forest, Linear Regression, XGBoost) |
| Interactive Dashboard | Power BI Desktop |
| Pivot Analysis | Microsoft Excel |
| Environment | Jupyter Notebook |

---

## 📁 Project Structure

```
wine-quality-analysis/
│
├── data/
│   ├── WineQT.csv                          # Raw dataset (UCI ML Repository)
│   └── cleaned_WineQT - Analyze.xlsx       # Cleaned & analysis-ready data
│
├── notebooks/
│   └── wine_quality_analysis.ipynb         # EDA, feature analysis, ML modeling
│
├── media/
│   ├── dashboard_preview.png               # Power BI dashboard screenshot
│   ├── excel_analysis.png                  # Excel pivot analysis screenshot
│   └── feature_importance.png             # Feature importance bar plot
│
├── presentation/
│   └── Finale-Ahmadi.pdf                  # Full project presentation (XDi Capstone)
│
└── README.md
```

---

## 📊 Dashboard Preview

![Wine Quality Analysis Dashboard](./media/Screenshot%202025-04-08%20143904b.jpg)
**Power BI Dashboard includes:**
- Average alcohol content by quality level (bar chart)
- Quality vs. alcohol vs. density (scatter plot)
- Average quality by pH (donut chart)
- Interactive slicers: Quality range · Alcohol range

**Excel Analysis includes:**
- Pivot table: average quality by feature
- Scatter plots: alcohol vs. quality, pH vs. quality
- Feature distribution charts

---

## 🔄 Analysis Workflow

```
Raw Data (UCI) → Cleaning & Inspection → EDA & Visualization →
Feature Engineering → ML Modeling (3 models) → Evaluation → Dashboard
```

**Python pipeline steps:**
1. Data loading and first inspection (`df.info()`, `df.describe()`)
2. Missing value check and outlier detection/treatment
3. Feature standardization (StandardScaler)
4. Train/test split (80/20)
5. Model training: Linear Regression · Random Forest · XGBoost
6. Evaluation: MSE · R² Score comparison
7. Feature Importance analysis
8. Export for Power BI & Excel visualization

---

## 📂 Dataset

| Field | Detail |
|-------|--------|
| Source | UCI Machine Learning Repository |
| Type | Red Wine (Vinho Verde) |
| Records | 1,143 samples |
| Target | Quality score (0–10 scale) |
| Features | fixed acidity · volatile acidity · citric acid · residual sugar · chlorides · free/total sulfur dioxide · density · pH · sulphates · alcohol |

---

## 🚀 How to Run

```bash
git clone https://github.com/Ahmadi-SeyedMohammadHossein/wine-quality-analysis
cd wine-quality-analysis
jupyter notebook notebooks/wine_quality_analysis.ipynb
```

**Power BI Dashboard:**
- Open any `.pbix` file in Power BI Desktop (free)

---

## 👤 Author

**Mohammad Hossein Ahmadi** — Certified Data Analyst | Frankfurt am Main, Deutschland  
*XDi Experience Design Institut — Capstone Project, April 2025*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin&logoColor=white)](https://linkedin.com/in/seyed-mohammad-hossein-ahmadi)
[![GitHub](https://img.shields.io/badge/GitHub-Portfolio-black?logo=github)](https://github.com/Ahmadi-SeyedMohammadHossein)
[![Email](https://img.shields.io/badge/Email-Contact-red?logo=microsoft-outlook&logoColor=white)](mailto:s.m.ahmadi@outlook.com)
