# Enterprise Resource Performance Analytics System (ERP-Integrated)

## Project Overview
This project implements an **ERP-integrated project performance analytics and decision support system** inspired by **SAP ERP project management workflows**.  
The goal is to analyze **resource utilization, cost efficiency, schedule adherence, and delivery risk** using data analytics and interpretable machine learning.

The solution is designed for **engineering managers, project managers, and PMO teams** to support **data-driven decision-making** across enterprise projects.

---

## ERP / SAP Business Context
In real-world enterprises, project-related data is stored across multiple ERP modules.  
This project simulates data extracted from SAP-style ERP systems, including:

- SAP PS (Project System)** – project timelines, milestones, delivery status  
- SAP CO (Controlling)** – budget allocation, cost usage  
- SAP HCM / SuccessFactors** – team size and experience  
- SAP Risk Management** – project risk classification  

The dataset represents **ERP project transaction data** analyzed outside the ERP system for advanced analytics and forecasting.

---

## End-to-End Data Flow

ERP Project Data (Simulated)
        ↓
Raw ERP Transactions (projects.csv)
        ↓
Data Cleaning & Validation
        ↓
Processed ERP Dataset
        ↓
Analytics & KPIs
        ↓
Machine Learning Risk Prediction
        ↓
Management Dashboard (Power BI)


## ERP System Architecture (Conceptual)

SAP ERP Modules (Simulated)
├── PS (Project System)
│   ├── Project timelines
│   ├── Milestones
│   └── Delivery status
│
├── CO (Controlling)
│   ├── Budget allocation
│   ├── Cost consumption
│   └── Budget variance
│
├── HCM / SuccessFactors
│   ├── Team size
│   ├── Team experience
│   └── Resource availability
│
├── Risk Management
│   ├── Risk level
│   └── Issue tracking
│
└── ERP Data Extract (CSV)
        ↓
Data Cleaning & Validation (Python)
        ↓
ERP Analytics Layer
├── KPIs & Trends
├── Resource Utilization Analysis
├── Cost & Schedule Analysis
        ↓
Machine Learning Layer
├── Delay Prediction Model
├── Risk Classification
        ↓
Visualization & Reporting
└── Power BI Executive Dashboard



---

## Dataset Description
- **Type:** Synthetic, industry-inspired ERP dataset  
- **Records:** 420 enterprise projects  
- **Domain:** Engineering & Project Management  

### Key Attributes
- Team Size & Experience  
- Estimated vs Actual Effort  
- Budget Usage & Resource Cost  
- Utilization Percentage  
- Issues Reported  
- Risk Level  
- Project Outcome (On-time / Delayed)  

The dataset intentionally includes **missing values** to reflect real ERP data quality challenges.

---

## Data Preparation & Feature Engineering
Key preprocessing steps:
- Handling missing numeric values using **median imputation**
- Handling missing categorical values using **most-frequent imputation**
- Encoding ERP categorical attributes (Project Type, Risk Level)
- Preparing analytics-ready and ML-ready datasets

Generated outputs:
- `projects_clean.csv`
- `projects_model_ready.csv`

---

## Exploratory Data Analysis & KPIs
Management-level KPIs derived from ERP data:
- On-Time Delivery Rate
- Budget Overrun Distribution
- Resource Utilization Trends
- Issue Frequency vs Project Delays
- Risk Level Impact on Delivery Outcomes

These KPIs help identify **early warning signals** during project execution.

---

## Analytics & Machine Learning Implementation

### Analytics
- Exploratory Data Analysis (EDA) performed using Python (Pandas, Seaborn, Matplotlib)
- Identified relationships between:
  - Budget usage and delays
  - Resource utilization and delivery risk
  - Issue escalation and project outcomes
- Results visualized using **Power BI dashboards** for management consumption.

### Machine Learning
- **Model Used:** Logistic Regression  
- **Objective:** Predict project delivery outcome (**Delayed / On-time**)  

### Why Logistic Regression?
- Interpretable and transparent
- Suitable for management decision support
- Commonly used in enterprise risk modeling

### ML Pipeline
- Missing value handling (numeric & categorical)
- Feature encoding using One-Hot Encoding
- Train-test split (80% / 20%)
- Model evaluation using:
  - Accuracy
  - Precision
  - Recall
  - Confusion Matrix

The ML model functions as an **ERP decision-support component**, providing early warnings for high-risk projects.

---

## Model Performance Summary
- **Accuracy:** ~77%
- Strong recall for delayed projects
- Suitable for **early-stage ERP risk prediction** and portfolio-level monitoring

---

## Business Value
This system enables organizations to:
- Detect delivery risks early
- Improve planning and estimation accuracy
- Optimize resource utilization
- Reduce budget overruns
- Strengthen ERP-driven project governance

---

## Tools & Technologies
- Python (Pandas, NumPy)
- Scikit-learn
- Jupyter / Google Colab
- Power BI (Web)
- ERP / SAP-inspired data modeling
- Git & GitHub

---

## Future Enhancements
- Integration with real SAP project exports
- Time-series forecasting for schedule risk
- Advanced ensemble ML models
- Automated ERP ETL pipelines


