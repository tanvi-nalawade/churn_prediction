# 📊 Customer Churn Prediction

A machine learning project that predicts whether a customer is likely to **churn (leave a company's service)** or **remain active**. The goal is to help businesses identify high-risk customers and take proactive retention measures.

## 🚀 Project Overview

Customer churn is a major challenge for subscription-based businesses. By analyzing customer demographics, account information, service usage, and billing details, this project builds machine learning models to predict the likelihood of customer churn.

The project covers the complete machine learning workflow:

**Data Collection → Data Cleaning → EDA → Feature Engineering → Model Training → Evaluation → Prediction → Deployment**

---

## ✨ Features

* Data preprocessing and cleaning
* Exploratory Data Analysis (EDA)
* Missing-value handling
* Categorical feature encoding
* Feature engineering
* Train-test data splitting
* Multiple machine learning models
* Model evaluation and comparison
* Churn probability prediction
* Confusion matrix and performance visualization
* Model serialization for deployment
* Optional Streamlit web application

---

## 🛠️ Technologies Used

### Programming Language

* Python 3.x

### Libraries

* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn

### Optional Technologies

* XGBoost
* Flask / FastAPI
* Streamlit
* SHAP / LIME

---

## 📂 Project Structure

```text
Customer-Churn-Prediction/
│
├── data/
│   └── churn_data.csv
│
├── notebooks/
│   └── EDA.ipynb
│
├── models/
│   └── churn_model.pkl
│
├── src/
│   ├── preprocessing.py
│   ├── train.py
│   └── predict.py
│
├── app.py
├── requirements.txt
├── README.md
└── LICENSE
```

---

## 📊 Dataset

The dataset contains customer-level information that can be used to identify patterns associated with churn.

### Example Features

| Feature          | Description                       |
| ---------------- | --------------------------------- |
| Customer ID      | Unique customer identifier        |
| Gender           | Customer gender                   |
| Age              | Customer age                      |
| Tenure           | Number of months with the company |
| Monthly Charges  | Customer's monthly bill           |
| Total Charges    | Total amount charged              |
| Contract Type    | Type of customer contract         |
| Internet Service | Internet service subscribed to    |
| Payment Method   | Customer payment method           |
| Churn            | Target variable                   |

### Target Variable

```text
0 → Customer stays
1 → Customer churns
```

---

## 🔍 Exploratory Data Analysis

The EDA phase focuses on understanding customer behavior and identifying factors associated with churn.

Key analyses include:

* Churn distribution
* Churn by gender
* Churn by age
* Churn by tenure
* Churn by contract type
* Churn by monthly charges
* Churn by internet service
* Churn by payment method
* Correlation analysis

Visualizations are created using **Matplotlib** and **Seaborn**.

---

## ⚙️ Machine Learning Workflow

### 1. Data Collection

Load the customer churn dataset using Pandas.

### 2. Data Cleaning

* Handle missing values
* Remove duplicate records
* Correct inconsistent data types
* Handle invalid or unnecessary values

### 3. Exploratory Data Analysis

Analyze customer characteristics and discover patterns related to churn.

### 4. Feature Engineering

Transform raw customer information into features suitable for machine learning.

Examples include:

* Encoding categorical variables
* Scaling numerical features
* Creating tenure groups
* Deriving additional customer-related features

### 5. Train-Test Split

The dataset is divided into training and testing sets.

```python
from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(
    X,
    y,
    test_size=0.2,
    random_state=42,
    stratify=y
)
```

### 6. Model Training

The project can compare multiple classification algorithms:

* Logistic Regression
* Decision Tree
* Random Forest
* Support Vector Machine
* XGBoost

### 7. Model Evaluation

Models are evaluated using:

* Accuracy
* Precision
* Recall
* F1-Score
* ROC-AUC
* Confusion Matrix

### 8. Prediction

The trained model predicts whether a new customer is likely to churn and can also provide a churn probability.

---

## 🤖 Models

### Logistic Regression

Provides a simple and interpretable baseline classification model.

### Decision Tree

Uses a tree-based structure to make classification decisions.

### Random Forest

Combines multiple decision trees to improve prediction performance and robustness.

### Support Vector Machine

Finds an optimal decision boundary between churn and non-churn customers.

### XGBoost

An optional gradient-boosting algorithm that can provide strong performance on structured/tabular data.

---

## 📈 Model Evaluation

Example evaluation output:

```text
Model: Random Forest

Accuracy:  0.XX
Precision: 0.XX
Recall:    0.XX
F1-Score:  0.XX
ROC-AUC:   0.XX
```

> The actual values should be added after training the models on the dataset.

A confusion matrix and ROC curve can also be generated to visually compare model performance.

---

## 🔮 Sample Prediction

### Customer Details

```text
Tenure: 18 months
Monthly Charges: 85.60
Contract: Month-to-Month
```

### Prediction

```text
Customer is likely to Churn.

Churn Probability: 91.3%
```

> This is an example output. The probability will depend on the trained model and input data.

---

## ▶️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/customer-churn-prediction.git
```

### 2. Navigate to the Project

```bash
cd customer-churn-prediction
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Usage

### Train the Model

```bash
python src/train.py
```

The trained model can then be saved inside the `models/` directory.

### Make Predictions

```bash
python src/predict.py
```

### Run the Streamlit Application

If a Streamlit interface is included:

```bash
streamlit run app.py
```

---

## 📦 Example `requirements.txt`

```text
pandas
numpy
scikit-learn
matplotlib
seaborn
jupyter
joblib
```

Optional dependencies:

```text
xgboost
streamlit
shap
```

---

## 💡 Business Impact

A churn prediction system can help businesses:

* Identify customers at high risk of leaving
* Prioritize retention campaigns
* Improve customer satisfaction
* Reduce customer acquisition costs
* Increase customer lifetime value
* Make data-driven retention decisions

---

## 🔮 Future Improvements

* Hyperparameter tuning using GridSearchCV or RandomizedSearchCV
* Cross-validation
* Advanced feature engineering
* XGBoost optimization
* Explainable AI using SHAP or LIME
* Real-time prediction API
* Streamlit dashboard
* Cloud deployment using AWS, Azure, or GCP
* Automated model retraining
* Customer segmentation
* Cost-sensitive churn prediction



## 👤 Author
Tanvi Nalawade 



## 🙏 Acknowledgements

* Scikit-learn Documentation
* Kaggle Customer Churn Dataset
* Python Open Source Community



