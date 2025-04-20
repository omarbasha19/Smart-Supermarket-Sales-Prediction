# Smart Supermarket Sales Prediction

## Overview
This project showcases a complete machine learning pipeline for analyzing and predicting supermarket sales behavior using the **CRISP-DM methodology**. The goal is to develop models that can support business decisions related to sales forecasting, payment method prediction, and customer satisfaction classification.

We used a real-world dataset containing detailed information about customer purchases across three branches, including demographics, transaction values, and product categories.

## Why CRISP-DM?
The project strictly follows the **CRISP-DM (Cross-Industry Standard Process for Data Mining)** framework to ensure a structured, business-oriented approach to problem solving.

---

## CRISP-DM Phases Applied

### 1. Business Understanding
- Understand business needs in the retail sector.
- Identify three key tasks: predicting total sales, payment method, and satisfaction level.

### 2. Data Understanding
- Explored and profiled 1,015 transactions across 3 branches.
- Performed visual and statistical analysis to identify variable distributions and initial correlations.

### 3. Data Preparation
- Removed duplicates and non-informative columns.
- Treated outliers using IQR and median replacement.
- Encoded categorical variables using Label Encoding and One-Hot Encoding.
- Applied Z-score normalization where needed.

### 4. Modeling
- Regression: Linear Regression, Decision Tree, Random Forest
- Classification: Decision Tree, Random Forest
- Used GridSearchCV for parameter optimization.
- Evaluation metrics: RMSE, MAE, R² (for regression) and Accuracy (for classification).

### 5. Evaluation
- Compared models across all tasks.
- Random Forest Regressor yielded the best results for predicting total sales (R² > 0.90).
- Payment prediction reached ~30% accuracy.
- Rating classification was more challenging due to weak correlation with available features.

### 6. Deployment (Proposal)
- Developed a function for interactive prediction.
- The model is ready to be integrated into a POS system via REST API or Streamlit application.

---

## Dataset Description
- Source: [Kaggle - Supermarket Sales Dataset](https://www.kaggle.com/datasets/faresashraf1001/supermarket-sales)
- Features include:
  - Customer demographics (Type, Gender)
  - Sales data (Quantity, Tax, Total)
  - Product and rating information
  - Payment method (Cash, Credit, Ewallet)
- Target variables:
  - `Total` (for regression)
  - `Payment` (for classification)
  - `Rating` (for satisfaction classification)

---

## Key Results

| Task                      | Best Model            | Score                   |
|---------------------------|------------------------|--------------------------|
| Total Sales Prediction    | Random Forest Regressor | R² ≈ 0.91, MAE < 0.1     |
| Payment Method Prediction | Random Forest Classifier | Accuracy ≈ 30%         |
| Rating Classification     | Decision Tree Classifier | Lower accuracy due to weak signal |

---

## Tools & Technologies
- Python, Jupyter Notebook
- pandas, numpy, matplotlib, seaborn
- scikit-learn, XGBoost
- GridSearchCV, LabelEncoder, StandardScaler

---

## Future Directions
- Include time-based features (e.g., time of purchase)
- Expand data with external variables (e.g., promotions, holidays)
- Improve rating classification using additional customer feedback
- Deploy as a real-time dashboard with user inputs

---

## Conclusion
This project demonstrates a full application of the CRISP-DM process to a real-world dataset. By combining business understanding with rigorous data science practices, we built interpretable and efficient models that can be directly applied to retail operations and customer engagement strategies.
