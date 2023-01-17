# Analyzing Customer Credit Risk

## Analysis Overview 

The purpose of this analysis was to use machine learning models to classify credit risk into 1 of 2 categories: good loans and risky loans. As in real world situation, good loans outnumber risky loans, a multitude of techniques were used to train and evaluate models used on the imbalanced dataset. Once each model's performance was evaluated, a decision was drawn to decide which model(s) to use to predict credit risk.

## Analysis Results: Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.
- Model 1, Naive Random Oversampling: 
  - Balanced accuracy score: 0.62
  - Precision: high-risk = 0.01, low-risk = 1.00
  - Recall: high-risk = 0.64, low-risk = 0.59
  
  [ins image]
  
- Model 2, SMOTE Oversampling: 
  - Balanced accuracy score: 0.62
  - Precision: high-risk = 0.01, low-risk = 1.00
  - Recall: high-risk = 0.64, low-risk = 0.59
  
  [ins image]
  
- Model 3, Random Undersampling: 
  - Balanced accuracy score: 0.61
  - Precision: high-risk = 0.01, low-risk = 1.00
  - Recall: high-risk = 0.67, low-risk = 0.55
  
  [ins image]
  
  
- Model 4, SMOTEENN: 
  - Balanced accuracy score: 0.60
  - Precision: high-risk = 0.01, low-risk = 1.00
  - Recall: high-risk = 0.72, low-risk = 0.48

  [ins image]
  
- Model 5, Balanced Random Forest Classifier: 
  - Balanced accuracy score: 0.77
  - Precision: high-risk = 0.03, low-risk = 1.00
  - Recall: high-risk = 0.63, low-risk = 0.91

  [ins image]
  
  
- Model 6, Easy Ensemble AdaBoost Classifier: 
  - Balanced accuracy score: 0.90
  - Precision: high-risk = 0.03, low-risk = 1.00
  - Recall: high-risk = 0.63, low-risk = 0.91

  [ins image]
  
## Summary of Findings 

Based on the results, the model with the highest accuracy is the Easy Ensemble AdaBoost Classifier model (accuracy = 0.90), and the model with the lowest accuracy is the SMOTEENN model (accuracy = 0.60). However, this accuracy score value is misleading, especially since the dataset is unbalanced. As shown by the imbalanced classification report, the precision and recall metrics for the high risk classification for all models are poor. This is an indication that there are a high number for false positives (low precision) and false negatives (low recall). This could have major implications as models with low precision are likely to classify low risk borrowers as high risk, and models with low recall are likely to classify high risk borrowers as low risk. This would be problematic as it would result in a higher likelihood that borrowers will default on their loans.
