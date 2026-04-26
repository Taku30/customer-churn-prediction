# customer-churn-prediction
Machine learning project to predict customer churn and identify key drivers using logistic regression and random forest.

# 📊 Customer Churn Prediction (Telecom Dataset)

A machine learning project to predict customer churn and identify key drivers of customer retention.

---

## 📌 Overview
Customer churn is a critical problem for telecom companies, as acquiring new customers is significantly more expensive than retaining existing ones.

This project analyzes customer behavior and builds predictive models to identify customers at risk of leaving, enabling targeted retention strategies.

---

## 🎯 Objectives
- Predict whether a customer will churn  
- Identify key factors driving churn  
- Compare model performance and select the most effective approach  

---

## 🧠 Models Used
- Logistic Regression (baseline)  
- Logistic Regression (class-weighted)  
- Random Forest (baseline and tuned)  

---

## ⚙️ Methodology

### Data Preprocessing
- Converted categorical variables using one-hot encoding  
- Handled missing values (TotalCharges)  
- Converted all features to numeric format  
- Split data into training and testing sets  
- Applied feature scaling for Logistic Regression  

### Handling Class Imbalance
- Used class_weight="balanced" to improve recall for churn prediction  

### Model Evaluation
Models were evaluated using:
- Accuracy  
- Precision  
- Recall  
- F1-score  

---

## 📈 Results

### Logistic Regression (Balanced)
- Recall for churn: ~0.75  
- Strong ability to identify at-risk customers  
- High interpretability through coefficients  

### Random Forest (Tuned)
- Similar performance to Logistic Regression  
- Captures non-linear relationships  
- Did not significantly outperform Logistic Regression  

👉 Final Decision:  
Logistic Regression was selected due to its interpretability and comparable performance.

---

## 🔍 Key Insights

- Customers with short tenure are significantly more likely to churn  
- Month-to-month contracts show the highest churn rates  
- Higher monthly charges are associated with increased churn  
- Fiber optic users tend to churn more, possibly due to higher expectations  

---

## 💼 Business Impact

- Focus retention efforts on new customers (low tenure)  
- Encourage long-term contracts to reduce churn  
- Improve service quality for high-paying customers  
- Use model predictions to proactively target high-risk customers  

---

## 📊 Feature Importance

Top drivers of churn (Random Forest):
- Tenure  
- Total Charges  
- Contract Type  
- Monthly Charges  
- Internet Service  

![Feature Importance](images/feature_importance.png)

---

## 📁 Project Structure

customer-churn-prediction/  
│── data/  
│── images/  
│── notebook/  
│── README.md  

---

## 🧩 Future Improvements
- Add ROC-AUC evaluation  
- Perform hyperparameter tuning (GridSearchCV)  
- Try Gradient Boosting / XGBoost  
- Deploy as a web application  

---

## 👤 Author
Taku Takahashi
