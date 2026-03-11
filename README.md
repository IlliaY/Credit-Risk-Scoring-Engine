# Credit Risk Scoring Engine

## Project Overview
This project builds a credit risk scoring engine to predict the probability of loan default using historical LendingClub data (2007-2018) (https://www.kaggle.com/datasets/wordsforthewise/lending-club). The goal is to assist in making data-driven lending decisions by optimizing for profitability and assessing risk under various economic scenarios.

## Key Features
- **Data Cleaning & Preprocessing**: Handling missing values, filtering relevant features, and encoding categorical variables.
- **Predictive Modeling**:
  - **Logistic Regression**: For baseline interpretability.
  - **Random Forest Classifier**: For capturing non-linear relationships and comparison to a "black(gray) box" model.
- **Business Impact Analysis**:
  - Calculation of expected profit based on loan terms and predicted default probabilities.
  - Threshold optimization to determine the best cutoff for approving loans.
- **Stress Testing**: Simulation of portfolio performance under different economic conditions:
  - Baseline (Normal)
  - Mild Recession (+50% defaults)
  - 2008 Crisis (+100% defaults)

## Dependencies
The project requires Python 3.10 and the following libraries:
- pandas
- numpy
- scikit-learn
- statsmodels
- matplotlib

## Results
The Random Forest model achieves an ROC-AUC score of approximately **0.68** which is worse than logistic regression model with ROC-AUC of **0.7**. The analysis further demonstrates how adjusting the probability threshold for loan rejection affects total portfolio profit, providing a tunable lever for risk management.

