# Customer Purchase Prediction using SVM

## Overview
This project predicts whether a customer will make a purchase based on two features:
- Age
- Estimated Salary

The goal is to compare multiple classification models and evaluate how kernel choice and regularization affect performance, particularly for imbalanced classes.

## Dataset
- Features: Age, EstimatedSalary
- Target: Purchased (0 = Not Purchased, 1 = Purchased)
- Notes:
  - Minor missing values were removed
  - Features were standardized prior to model training
  - Dataset is not included due to licensing/academic restrictions

## Methods
The following models were trained and evaluated using cross-validation:
- LinearSVC (hinge loss)
- SVC with linear kernel
- SGDClassifier (hinge loss)
- SVC with RBF kernel
- Tuned SVC (RBF) using RandomizedSearchCV

Evaluation metrics:
- Accuracy
- Precision
- Recall
- Confusion Matrix

## Key Findings
- Linear models performed reasonably well but showed limited recall for the positive class
- The RBF kernel significantly improved recall while maintaining similar accuracy
- Hyperparameter tuning slightly increased precision but introduced signs of overfitting
- The untuned RBF SVC achieved the best balance of performance

## Final Model Performance (Test Set)
- Accuracy: 90%
- Precision: 91%
- Recall: 90%

These results indicate good generalization and no significant overfitting.

## Example Predictions
The final model was used to predict purchase behavior for three hypothetical individuals:
- Age 25, Salary 60,000 → Not Purchased
- Age 40, Salary 80,000 → Not Purchased
- Age 50, Salary 120,000 → Purchased

## Tools
- Python
- pandas, numpy
- scikit-learn
- matplotlib

## Notes
This project was originally developed as part of an academic assignment and has been refactored for portfolio presentation.
