# Airline Customer Satisfaction - Model Evaluation Project
## Project Overview
This project analyzes passenge survey data using Python and Scikit-learn to buid and evaluate predictive models for airline customer satisfaction. It compares an optimized Decision Tree Classifier agianst a baseline Logistic Regression model to provide transparent, actionable recommendations for airline management.
## Dataset Summary
***Source Dataset:**
'Invistico_Airline.csv'
***Observations:** 129,880 rows
***Features:** 22 operational and demographic columns
***Target Variable:** 'satisfied' (Binary:1 = Satisfied, 0 = Dissatisfied)
## Hyperparameter Tuning Strategy
GridSearchCV was used with 3-fold cross-validation strategy to optimize the Decision Tree structure and prevent overfitting.
***Best Hyperparameters Found:**
* 'max_depth': 10
* 'min_samples_leaf': 1
## Model Performance Comparison
| Model Metric | Decision Tree Classifier | Logistic Regression |
| :--- | :--- | :---
| **Overall Accuracy** | **92.00% | **83.00% |
| **F1-Score ("Satisfied")** | **0.9275** | **0.8436** |
### Business & Analytical Rationale
The Decision Tree significantly outperformed Logistic Regression. Airline customer satisfaction features interact non-linearly (e.g., *Inflight Entertainment* quality matters exponentially more on long-haul flights than short ones). Decision Trees naturally map these complex interaction pathways, whereras Logistic Regression assumes rigid linear relationships.
## Top Operational Drivers of Satisfaction
Based on the trained Decision Tree feature importance calculation, the top 3 items to target for service improvrments are:
1. **Inflight Entertainment** (Highest impact on satisfaction scores)
2.**Seat Comfort**
3. **Ease of Online Booking**
## Business Actionability for Management
***Strategic Spending:** Management should prioritize capital allocation toward upgraded inflight entertainment software and seating ergonomics to yield the highest possible return on customer retention.
***Auditability:** The visual decision pathways allow customer service managers to easily audit why specific demographicss risk without requiring technical programming knowledge.