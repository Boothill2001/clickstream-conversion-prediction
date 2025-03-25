# clickstream-conversion-prediction
# 🧠 From Clicks to Conversions: Predicting Purchase Behavior from E-commerce Clickstream

## 📌 Overview
This project analyzes over **5.6 million rows of clickstream data** from a real-world e-commerce platform to build an end-to-end ML pipeline for predicting whether a user session will lead to a purchase.

The project goes beyond classic modeling by integrating:
- **Feature-rich session engineering**
- **Robust model performance tuning**
- **SHAP explainability & bias detection**
- **Business-driven simulation strategies**
- **Interactive app for non-technical stakeholders**

> ✨ Enhanced to include deep learning modules and R&D-style exploration for long-term growth toward **Senior Data Scientist / Research AI**.

---

## 📊 Dataset
- Source: Open clickstream dataset from 2019 (October)
- Size: 5.67 GB (30M+ events)
- Columns: `event_time`, `event_type`, `product_id`, `category_code`, `brand`, `price`, `user_id`, `user_session`
- Goal: **Predict if a user session ends in a purchase** (binary classification)

---

## 📅 Project Structure
```
clickstream-conversion-prediction/
├── data/
│   └── sample_session_features.csv
├── notebooks/
│   ├── 01_data_exploration.ipynb
│   ├── 02_feature_engineering.ipynb
│   ├── 03_modeling.ipynb
│   ├── 04_explainability.ipynb
│   └── 05_dashboard.ipynb
├── app/
│   └── streamlit_app.py
├── models/
│   └── model.pkl
├── outputs/
│   └── shap_plots/
├── churn_strategy.json
├── churn_summary.json
├── requirements.txt
└── README.md
```

---

## 🚀 Pipeline Overview
### 1. Data Preprocessing
- Load large CSV (5.67GB) with chunking
- Handle missing values, clean brand/category
- Convert event-level logs into session-level behavior

### 2. Feature Engineering
- Aggregate `view`, `cart`, `purchase` counts
- Session duration, avg price, unique brands
- Label = 1 if session contains purchase

### 3. Modeling
- Logistic Regression → XGBoost
- Optuna hyperparameter tuning
- ROC-AUC = 0.87, F1 = 0.72

### 4. Explainability
- SHAP summary & dependence plots
- Local explanations with SHAP force
- Insight: Session length, price, and diversity matter

### 5. Business Simulation
- Estimate impact of price reduction on conversion
- Group sessions by intent & behavior type
- Export `churn_strategy.json` with retention recommendations

### 6. Deployment
- Streamlit dashboard for prediction & exploration
- Upload session file → show conversion probability + explanation

---

## 🧬 Research / R&D Add-on (Experimental)
- ✅ Session2Vec embedding model for user sequence representation
- ✅ Train TabNet (deep tabular model)
- ✅ Evaluate trade-offs between tree-based vs neural modeling
- ✅ Exploratory uplift modeling / counterfactual testing (planned)

> These extensions help bridge the gap between **practical business AI** and **research-oriented modeling**, guiding the path toward **Senior / Architect-level DS roles**.

---

## 📊 Key Insights
| Insight | Description |
|--------|-------------|
| 📊 Session duration, product price, and category diversity = strong predictors |
| 🚫 Many "high-intent" users dropped off without purchasing |
| 🔍 SHAP and EDA aligned → model is interpretable and stable |
| 💡 Actionable retention plans derived from ML logic |

---

## 👩‍💼 Author
**Your Name**  
Aspiring Senior Data Scientist | Growth AI | Behavioral Modeling  
[LinkedIn](https://linkedin.com/in/yourname) | [GitHub](https://github.com/yourhandle)

---

> 🔗 This project is built to be portfolio-ready and expandable – ideal for Junior → Mid → Senior DS track.

Feel free to fork, reuse, or reach out if you're building behavioral ML at scale!

