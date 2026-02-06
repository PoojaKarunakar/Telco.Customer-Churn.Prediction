
#  Telco Customer Churn Prediction

A complete **Machine Learning pipeline** for predicting customer churn using the **Telco Customer Churn dataset** (Kaggle).  
The project includes full preprocessing, feature selection, model comparison (including XGBoost), and performance visualization.

---

##  Project Overview

This project aims to predict whether a telecom customer is likely to **churn (leave the service)** based on demographic and usage data.  
By understanding key churn drivers, telecom companies can improve retention and customer experience.

---

##  Workflow Summary

###  1. Data Loading & Cleaning
- Loaded Telco dataset (`telc.csv`)
- Converted `TotalCharges` from obeject to float
- Handled missing values and incorrect data types
- Encoded the target variable `Churn` as binary (0 = No, 1 = Yes)

###  2. Exploratory Data Analysis (EDA)
- Visualized churn distribution  
- Examined relationships with categorical features
- Correlation heatmap to identify strong predictors

###  3. Feature Engineering
- Used **LAbel-Encoding** for categorical variables  
- Scaled numeric features using **StandardScaler**  
- Selected top 20 important features using **Random Forest feature importances**

###  4. Model Training & Evaluation
Trained and compared multiple algorithms:
- **Decision Tree**
- **Random Forest**
- **XGBoost** *(if available)*

Each model was evaluated using:
- Accuracy  
- Precision  
- Recall  
- F1 Score  
- AUC (Area Under the ROC Curve)

###  5. Visualization
- Churn distribution plots  
- Confusion Matrix for best model  
- ROC Curve visualization  
- Feature importance bar chart  

###  6. Optimization & Saving
- Optimized memory usage by converting data types  
- Saved the trained scaler and best model with **Joblib**

---

##  Results

| Model | Accuracy | Precision | Recall | F1 | AUC |
|-------|-----------|-----------|--------|----|-----|
| Decision Tree | ~82% | - | - | - | - |
|**Random** Forest |**~84%** | - | - | - | **Best** |
| XGBoost | ~82% | - | - | - |  |

> Random Forest achieved the highest AUC and overall performance.

---

##  Tech Stack

| Library | Purpose |
|----------|----------|
| **Python 3.x** | Core language |
| **Pandas / NumPy** | Data manipulation |
| **Matplotlib / Seaborn** | Visualization |
| **Scikit-learn** | ML models & metrics |
| **XGBoost** | Gradient boosting |
| **Joblib** | Model persistence |

---

##  How to Run

 **Clone this repository**
   ```bash
  https://github.com/PoojaKarunakar/Telco.Customer-Churn.Prediction
````


---

##  Insights

* Customers on **month-to-month contracts** had the highest churn rates.
* **Electronic check payments** correlated strongly with churn.
* **Longer tenure** and **automatic payments** were indicators of retention.

---

##  Saved Outputs

| File                     | Description                       |
| ------------------------ | --------------------------------- |
| `scaler.pkl`             | Fitted StandardScaler             |
| `model.pkl` | Best performing model             |
|`encoders.pk1`        | Stores encoding values |

---

##  Future Improvements

* Implement **GridSearchCV** for hyperparameter tuning
* Add **cross-validation** for more robust evaluation
* Deploy model via **Flask API**

---

##  Author

**Pooja**
Data Science & Machine Learning Enthusiast


*If you find this useful, please star the repository on GitHub!* 


📌 Outcome

The final model effectively predicts customer churn and provides insights that can support data-driven retention strategies.

│
[Telco Customer Churn Dataset](https://raw.githubusercontent.com/PoojaKarunakar/Telco.Customer-Churn.Prediction/main/Telco-Customer-Churn-Dataset.csv)-- telco_customer_churn.csv
<br>
<br>
│
[Telco Customer Churn jpynb](https://github.com/PoojaKarunakar/Telco.Customer-Churn.Prediction/blob/main/telco.Customer%20Churn.project.ipynb)---telco.Customer Churn.ipynb
│  
<br>
│
├── screenshots <br>
│   ├── [roc_curve.png](https://github.com/PoojaKarunakar/Telco.Customer-Churn.Prediction/blob/main/AUC.png)
  <br>
│   └── [accuracy.png](https://github.com/PoojaKarunakar/Telco.Customer-Churn.Prediction/blob/main/random%20forest.png)


