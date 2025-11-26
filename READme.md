# **Loblaws Customer Churn Prediction – Assignment 4**

## **1. Introduction**
This project develops a machine learning model to predict customer churn for Loblaws Digital. It supports data-driven retention by identifying customers at high risk of leaving and integrating model outputs with CRM and marketing platforms. The system architecture includes data ingestion, preprocessing, model inference, and automated workflows for real-time decision-making.

---

## **2. Project Structure**


CHURN_PREDICTION_LOBLOWS/
│
├── .gitignore
├── venv/ # Virtual environment
│
├── churn prediction flowchaart.png # Integration flowchart diagram
├── churn_prediction.html # Executed HTML version of the notebook
├── churn_prediction.ipynb # Full Jupyter notebook
├── loblaws.xlsx # Raw customer dataset
│
├── scaler.pkl # Preprocessing scaler
├── xgb_best_model.pkl # Final trained XGBoost model
├── xgb_shap_model.json # SHAP-compatible XGBoost model
│
├── requirements.txt # Python dependency list
└── README.md

---

## **3. How to Use**

### **Run the Notebook**

**Open the notebook in Jupyter Notebook or VS Code:**

`jupyter notebook churn_prediction.ipynb`

**Load the Model Files**

**Use these artifacts for predictions without retraining:**

- scaler.pkl — preprocessing transformer
- xgb_best_model.pkl — final trained churn prediction model
- xgb_shap_model.json — for SHAP explainability
----
Example code:
import pickle
import xgboost as xgb

scaler = pickle.load(open("scaler.pkl", "rb"))
model = pickle.load(open("xgb_best_model.pkl", "rb"))

---

## **4. Integration Architecture**

- **Data Ingestion:**  
  Customer behavioral and transactional data is extracted from internal systems and transformed for model-ready use.

- **Model Inference API:**  
  A lightweight REST API exposes the churn model for real-time scoring.

- **CRM & Marketing Integration:**  
  Predictions feed into CRM platforms and automation tools (e.g., email, loyalty campaigns) to trigger retention actions.

- **Monitoring & Updates:**  
  Automated pipelines track model drift, performance metrics, and trigger periodic retraining to maintain accuracy.

---

## **5. Tech Stack**
- requirements.txt
**Tools & Platforms:**  
- Jupyter Notebook  

---

## **6. Authors**
- Hasyashri Bhatt  
- Baban  
- Fenil  
- Shrinu  
---

## **7. License**
This project is part of an academic course assignment and is **not intended for commercial use**. All data and code are original student work unless otherwise referenced.
