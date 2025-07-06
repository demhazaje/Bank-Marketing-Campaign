# 📊 Bank Marketing Campaign - Term Deposit Subscription Prediction

This project uses machine learning to predict whether a customer will subscribe to a term deposit following a phone-based marketing campaign by a Portuguese bank.

---

## 📁 Project Structure

├── data/ # Raw data files

├── Bank_Campaign.ipynb # Jupyter Notebook with full EDA, modeling, and evaluation

├── README.md # Project overview and documentation

└── requirements.txt # Required libraries


---

## 🎯 Business Objective

The goal of this project is to help the bank:
- **Identify high-potential leads** for term deposit subscription.
- **Improve campaign efficiency** by reducing unnecessary calls.
- **Increase return on investment (ROI)** for marketing campaigns using predictive analytics.

---

## 🧹 Data Cleaning & Preparation

- Handled `'unknown'` values by replacing them with column-wise mode.
- Dropped the `pdays` column due to uninformative entries (mostly 999).
- Encoded categorical features using `.map()` to avoid issues during testing.
- Scaled numerical features using `StandardScaler`.

---

## ⚖️ Class Imbalance Handling

- Only ~11% of customers subscribed.
- Used **SMOTE (Synthetic Minority Oversampling Technique)** to balance the training data.

---

## 🤖 Models Implemented

| Model                | Tuned with GridSearchCV | Key Metrics Evaluated |
|----------------------|--------------------------|------------------------|
| K-Nearest Neighbors  | ✅                       | Accuracy, F1, AUC      |
| Decision Tree        | ✅                       | Accuracy, F1, AUC      |
| Random Forest        | ✅                       | Accuracy, F1, AUC      |
| XGBoost Classifier   | ✅                       | Accuracy, F1, AUC      |

> Evaluation focused on **F1 Score** and **Recall**, given the importance of identifying as many potential subscribers as possible.

---

## 🏆 Model Performance Summary (Test Set)

| Model         | Accuracy | Precision | Recall | F1 Score | ROC AUC |
|---------------|----------|-----------|--------|----------|---------|
| **XGBoost**   | 91.00%   | 58.03%    | 72.84% | 64.60%   | 83.08%  |
| Random Forest | 90.86%   | 57.64%    | 71.12% | 63.68%   | 82.24%  |
| Decision Tree | 88.53%   | 49.28%    | 62.72% | 55.19%   | 77.26%  |
| KNN (k=2)     | 88.09%   | 47.35%    | 51.08% | 49.14%   | 71.93%  |

---

## 📌 Key Takeaways

- **XGBoost performed best** across all key metrics.
- Duration of call, previous campaign outcome, and month of contact were top predictors.
- ML-powered targeting can significantly improve campaign efficiency and customer conversion.

---

## 🧠 Business & Managerial Implications

- Prioritize customers with higher predicted likelihood for term deposit subscriptions.
- Reduce campaign size and cost while maintaining effectiveness.
- Use feature importance and explainable AI (e.g., SHAP) to drive strategic decisions.

---

## 📂 Access the Project

- 🔗 **Kaggle Notebook**: [View Here](https://www.kaggle.com/code/demhazaje/bank-campaign)
- 💻 **GitHub Repository**: [View Codebase](https://github.com/demhazaje/Bank-Marketing-Campaign)

---

## 🚀 Future Enhancements

- Use SHAP/LIME for model explainability.
- Build real-time lead scoring system.
- Add features like income, region, or customer tenure.

---

## 📦 Requirements

To install the required libraries:

bash
pip install -r requirements.txt

--- 


## 🙌 Acknowledgments

Dataset sourced from:

- [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/222/bank+marketing)  
- [Kaggle Dataset](https://www.kaggle.com/datasets/pankajbhowmik/bank-marketing-campaign-subscriptions/data)

---

## 📬 Connect

If you have suggestions or feedback, feel free to [open an issue](https://github.com/demhazaje/Bank-Marketing-Campaign/issues) or connect with me on [LinkedIn](https://www.linkedin.com/in/ejazahmed7/).





