# credit-risk-classification
# Overview of the Analysis

## Purpose of the Analysis

The analysis aimed to develop and assess machine learning models for credit risk analysis, predicting whether a loan is healthy (0) or poses a high risk of default (1) based on financial information.

## Financial Information and Prediction Target

The dataset included financial details of loans, and the target variable was "loan_status," where 0 signifies a healthy loan, and 1 indicates a high-risk loan.

## Basic Information about Variables

To grasp label distribution, the `value_counts()` method tallied occurrences of each label. The data revealed an imbalance, with significantly more healthy loans (0) than high-risk loans (1).

## Stages of the Machine Learning Process

1. **Data Loading:** Lending data was loaded from a CSV file.
2. **Data Preprocessing:** Labels and features were created, and data was split into training and testing sets.
3. **Model Building:** Logistic regression models were employed with both original and resampled data.
4. **Model Evaluation:** Accuracy, confusion matrices, and classification reports were calculated.

## Methods Used

Logistic regression served as the primary classification algorithm. Additionally, RandomOverSampler from the imbalanced-learn library addressed data imbalance.

# Results

## Machine Learning Model 1: Logistic Regression (Original Data)

- Accuracy Score: 0.99
- Precision and Recall for Label 0 (Healthy Loan): 1.00
- Precision for Label 1 (High-Risk Loan): 0.87
- Recall for Label 1 (High-Risk Loan): 0.89

## Machine Learning Model 2: Logistic Regression (Resampled Data)

- Accuracy Score: 1.00
- Precision and Recall for Label 0 (Healthy Loan): 1.00
- Precision for Label 1 (High-Risk Loan): 0.87
- Recall for Label 1 (High-Risk Loan): 1.00

# Summary

## Model Performance

- Both models demonstrated high accuracy, with the resampled model achieving a perfect score.
- The resampled model showed improved recall for high-risk loans compared to the original model.

## Recommendation

Considering the excellent performance:

- If a balanced approach is needed, the resampled model is recommended for its perfect accuracy and balanced recall.
- If precision is crucial, and high-risk loans require higher confidence, the original model may be considered.

The choice may depend on business priorities and the precision-recall trade-off.

In conclusion, both models are strong candidates, and the selection should align with business objectives and preferences for handling false positives and false negatives. The resampled model offers a balanced solution in the absence of a clear preference.

