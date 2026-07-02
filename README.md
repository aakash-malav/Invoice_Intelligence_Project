# 📦 Vendor Invoice Intelligence Portal

An end-to-end Machine Learning project that predicts vendor invoice freight costs and automatically flags high-risk invoices for manual approval. The project integrates PostgreSQL, Python, SQL, Scikit-learn, and Streamlit to build an intelligent procurement analytics application.

---

## 📖 Project Overview

Managing vendor invoices manually can be time-consuming and prone to human error. This project automates two critical finance operations:

1. **Freight Cost Prediction**
   - Predicts the expected freight cost for a vendor invoice based on invoice value.
   - Helps procurement teams estimate logistics costs before invoice approval.

2. **Invoice Risk Flagging**
   - Identifies invoices that should be manually reviewed based on abnormal invoice characteristics.
   - Reduces financial leakage and improves operational efficiency.

The final solution is deployed as an interactive Streamlit web application where users can make real-time predictions.

---

## 🚀 Features

### 📦 Freight Cost Prediction
- Predict freight cost using Machine Learning
- Regression-based prediction
- Real-time prediction through Streamlit interface

### 🚩 Invoice Risk Flagging
- Binary classification model
- Detects invoices requiring manual approval
- Real-time risk prediction

### 💾 Database Integration
- PostgreSQL database
- SQL-based feature engineering
- Environment variables for secure credentials

### 🌐 Web Application
- Interactive Streamlit dashboard
- User-friendly interface
- Instant predictions

---

## 🛠️ Tech Stack

### Programming Language
- Python

### Database
- PostgreSQL

### Machine Learning
- Scikit-learn

### Data Processing
- Pandas
- NumPy

### Visualization
- Plotly
- Streamlit

### Model Serialization
- Joblib

### Database Connectivity
- SQLAlchemy
- psycopg2

### Environment Management
- python-dotenv

---

## 📂 Project Structure

```
Vendor_Invoice_Intelligence_Project/
│
├── app.py
├── .env
├── .gitignore
├── requirements.txt
│
├── Freight_cost_prediction/
│   ├── data_preprocessing.py
│   ├── modeling_evaluation.py
│   ├── train.py
│
├── invoice_flagging/
│   ├── data_preprocessing.py
│   ├── modeling_evaluation.py
│   ├── train.py
│
├── inference/
│   ├── predict_freight.py
│   ├── predict_invoice_flag.py
│
├── models/
│   ├── predict_freight_model.pkl
│   ├── predict_flag_invoice.pkl
│   └── scaler.pkl
│
└── README.md
```

---

## 📊 Dataset

The project uses an inventory and vendor invoice dataset stored in PostgreSQL consisting of:

- Purchases
- Vendor Invoice
- Purchase Prices
- Beginning Inventory
- Ending Inventory

The original SQLite database was migrated to PostgreSQL for improved scalability and production readiness.

---

## 🔧 Feature Engineering

### Freight Cost Prediction

Input Feature:

- Invoice Dollars

Target:

- Freight Cost

---

### Invoice Risk Flagging

Features:

- Invoice Quantity
- Invoice Dollars
- Freight
- Total Item Quantity
- Total Item Dollars

Target:

- Flag Invoice (0 = Safe, 1 = Manual Approval Required)

Additional features were engineered using SQL:

- Total Brands
- Total Item Quantity
- Total Item Dollars
- Average Receiving Delay
- Days from PO to Invoice
- Days to Pay

---

## 🤖 Machine Learning Models

### Freight Cost Prediction

Regression Models

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor

Evaluation Metrics

- MAE
- RMSE
- R² Score

---

### Invoice Risk Flagging

Classification Models

- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier

Hyperparameter tuning performed using GridSearchCV.

Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1 Score
- Classification Report

---

## 🗄 SQL Operations

The project performs SQL-based feature engineering including:

- Aggregations
- GROUP BY
- LEFT JOIN
- Common Table Expressions (CTE)
- Date calculations
- Feature creation

---

## 🔐 Environment Variables

Database credentials are securely stored using a `.env` file.

Example:

```env
POSTGRES_USER=postgres
POSTGRES_PASSWORD=your_password
POSTGRES_HOST=localhost
POSTGRES_PORT=5432
POSTGRES_DB=inventory
```

---

## ▶️ Running the Project

### 1. Clone Repository

```bash
git clone https://github.com/yourusername/vendor-invoice-intelligence.git
```

---

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

---

### 3. Configure Environment Variables

Create a `.env` file with PostgreSQL credentials.

---

### 4. Train Models

Freight Prediction

```bash
python Freight_cost_prediction/train.py
```

Invoice Flagging

```bash
python invoice_flagging/train.py
```

---

### 5. Launch Streamlit Application

```bash
streamlit run app.py
```

---

## 📈 Application Workflow

```
PostgreSQL Database
        │
        ▼
SQL Feature Engineering
        │
        ▼
Data Preprocessing
        │
        ▼
Model Training
        │
        ▼
Save Model (.pkl)
        │
        ▼
Inference Module
        │
        ▼
Streamlit Dashboard
        │
        ▼
Real-Time Prediction
```

---

## 📷 Application Modules

### Freight Cost Prediction

- Input Invoice Dollars
- Predict Estimated Freight Cost

### Invoice Manual Approval

- Input Invoice Details
- Predict Safe / Manual Approval Required

---

## 🔮 Future Improvements

- Docker deployment
- Cloud deployment (AWS/Azure)
- REST API using FastAPI
- Explainable AI using SHAP
- Automated model retraining
- Vendor performance dashboard
- Fraud detection analytics

---

## 📚 Libraries Used

- pandas
- numpy
- scikit-learn
- sqlalchemy
- psycopg2
- python-dotenv
- streamlit
- plotly
- joblib

---

## 👨‍💻 Author

**Aakash Malav**

MBA Candidate | IIM Rohtak

Interested in Machine Learning, Data Analytics, Finance, and AI-driven Business Solutions.

---
