# Enterprise Resource Performance Analytics System

## Project Overview
This project simulates a real-world enterprise project analytics system that analyzes
resource utilization, cost efficiency, and project outcomes using data analytics and
machine learning.

The goal is to predict whether a project will be **Delayed** or **On-time** based on
resource, budget, and team-related factors.

---

## Dataset
- Synthetic, industry-inspired dataset
- 420 enterprise projects
- Includes missing values to reflect real-world uncertainty

### Key Features
- Team Size
- Team Experience
- Budget Usage %
- Resource Cost
- Utilization %
- Issues Reported
- Risk Level

Target Variable:
- **Outcome** (Delayed / On-time)

---

## Data Processing
- Missing values handled using median (numerical) and most-frequent (categorical)
- Categorical features encoded using One-Hot Encoding
- Feature scaling applied where required
- Train-test split: 80% / 20%

---

## Machine Learning Model
- Model: Logistic Regression
- Pipeline used for preprocessing + modeling
- Evaluation Metrics:
  - Accuracy
  - Precision
  - Recall
  - F1-score
  - Confusion Matrix

---

## Results
- Overall Accuracy: **~77%**
- Strong recall for delayed projects
- Demonstrates realistic enterprise risk prediction behavior

---

## Tools & Technologies
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib / Seaborn
- Google Colab

---

## Business Use Case
This system can help:
- Project Managers identify high-risk projects early
- Organizations optimize resource allocation
- Leadership make data-driven delivery decisions
