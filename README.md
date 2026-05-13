# 🏥 Medical Insurance Churn Prediction

This project leverages machine learning techniques to predict potential customer churn in the medical insurance domain, using the [Medical Cost Personal Dataset](https://www.kaggle.com/datasets/mirichoi0218/insurance). We consider **high medical charges** as a proxy for **churn risk**, assuming that users with high costs may be at greater risk of canceling or lapsing their insurance coverage.

---

## 📁 Project Structure

```
Churn_Prediction/
│
├── Churn_Prediction.ipynb       # Main Jupyter notebook
├── insurance.csv                # Dataset (uploaded from Kaggle)
└── README.md                    # Project documentation (this file)
```

---

## 📌 Problem Statement

**Goal:** Predict whether a customer is at risk of churning (proxy: `charges` > median) based on features like age, BMI, smoking status, region, etc.

---

## 🧠 Project Workflow

### 1. Exploratory Data Analysis (EDA)
- Distribution of key features (`age`, `bmi`, `charges`, etc.)
- Correlation heatmap to understand relationships
- Visualization by smoker, region, children, and churn status

### 2. Data Preprocessing
- Categorical encoding using One-Hot Encoding
- BMI binning (underweight, healthy, overweight, obese)
- Created new binary target variable: `churn_risk` = 1 if charges > median
- Created many visualisations

### 3. Model Building
Tried out and tuned the following classification models:
- ✅ Logistic Regression
- ✅ Random Forest Classifier
- ✅ XGBoost Classifier

### 4. Evaluation
Metrics used:
- Accuracy
- Precision
- Recall
- F1-Score
- ROC AUC Curve


---

## 📊 Key Results

Model                 Accuracy	         ROC-AUC
Logistic Regression	  0.910448	         0.911745
Random Forest	        0.932836	         0.930272
XGBoost	              0.925373	         0.922749

> Random Forest performed best.

---

## 🔍 Final Conclusion

- **Smoking status** and **BMI** are top predictors of high insurance charges.
- The churn risk model can help insurance companies **proactively retain customers** by identifying high-risk profiles.
- Logistic Regression is interpretable, but **Random Forest** provides the best performance.
- Further improvements could include adding more behavioral or historical features.

---

## ▶️ How to Run

1. Clone the repo or download the files.
2. Install required packages:
   ```bash
   pip install -r requirements.txt
   ```
3. Open the notebook:
   ```bash
   jupyter notebook Churn_Prediction.ipynb
   ```

---

## 📄 License

MIT — see [LICENSE](LICENSE).

---

## 📦 Requirements

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- xgboost
- jupyter




