# Analyzing Customer Credit Risk

## Analysis Overview 

The purpose of this analysis was to use machine learning models to classify credit risk into 1 of 2 categories: good loans and risky loans. As in real world situation, good loans outnumber risky loans, a multitude of techniques were used to train and evaluate models used on the imbalanced dataset. Once each model's performance was evaluated, a decision was drawn to decide which model(s) to use to predict credit risk.

## Analysis Results
- Model 1, Naive Random Oversampling: 
  - Balanced accuracy score: 0.62
  - Precision: high-risk = 0.01, low-risk = 1.00
  - Recall: high-risk = 0.64, low-risk = 0.59
  
 ![ins1](https://user-images.githubusercontent.com/96188669/212809549-8e7e8445-cf74-4260-8120-4d5a69ae5c08.png)

 ![ins1 1](https://user-images.githubusercontent.com/96188669/212809593-e4db5a89-fad6-424b-a697-fe97105982de.png)
 
  
- Model 2, SMOTE Oversampling: 
  - Balanced accuracy score: 0.62
  - Precision: high-risk = 0.01, low-risk = 1.00
  - Recall: high-risk = 0.64, low-risk = 0.59
  
 ![ins2](https://user-images.githubusercontent.com/96188669/212809611-b804bec5-4c6d-4605-8470-e08666ef8208.png)

 ![ins2 1](https://user-images.githubusercontent.com/96188669/212809646-a8c46160-344c-4e5d-a5a3-6665271bb4f4.png)


- Model 3, Random Undersampling: 
  - Balanced accuracy score: 0.61
  - Precision: high-risk = 0.01, low-risk = 1.00
  - Recall: high-risk = 0.67, low-risk = 0.55
  
 ![ins3](https://user-images.githubusercontent.com/96188669/212809681-80fda184-707e-4b60-a368-24e65e1b2fa6.png)

 ![ins3 1](https://user-images.githubusercontent.com/96188669/212809694-86946f32-f0ae-4164-8ae0-1488ab3eac5b.png)
  
  
- Model 4, SMOTEENN: 
  - Balanced accuracy score: 0.60
  - Precision: high-risk = 0.01, low-risk = 1.00
  - Recall: high-risk = 0.72, low-risk = 0.48

 ![ins4](https://user-images.githubusercontent.com/96188669/212809718-ee95fcc0-b4ba-490b-8767-249d86623dab.png)
 
 ![ins4 1](https://user-images.githubusercontent.com/96188669/212809735-df74a691-f7c0-4081-a31b-66dc00c1b489.png)

  
- Model 5, Balanced Random Forest Classifier: 
  - Balanced accuracy score: 0.77
  - Precision: high-risk = 0.03, low-risk = 1.00
  - Recall: high-risk = 0.63, low-risk = 0.91

 ![ins5](https://user-images.githubusercontent.com/96188669/212809798-10c882fb-3ac3-4b63-9d2b-32ff8be0c3f5.png)

 ![ins5 1](https://user-images.githubusercontent.com/96188669/212809832-f5215325-f5fc-4db7-9894-cea1e27baebb.png)

  
- Model 6, Easy Ensemble AdaBoost Classifier: 
  - Balanced accuracy score: 0.90
  - Precision: high-risk = 0.03, low-risk = 1.00
  - Recall: high-risk = 0.63, low-risk = 0.91

 ![ins6](https://user-images.githubusercontent.com/96188669/212809850-48de5462-615e-4a94-9da6-bcfe41e1caac.png)

 ![ins6 1](https://user-images.githubusercontent.com/96188669/212809924-df768e3b-9f6a-426b-8f5c-125f6ec0b5fa.png)

  
## Summary of Findings 

Based on the results, the model with the highest accuracy is the Easy Ensemble AdaBoost Classifier model (accuracy = 0.90), and the model with the lowest accuracy is the SMOTEENN model (accuracy = 0.60). However, this accuracy score value is misleading, especially since the dataset is unbalanced. As shown by the imbalanced classification report, the precision and recall metrics for the high risk classification for all models are poor. This is an indication that there are a high number for false positives (low precision) and false negatives (low recall). This could have major implications as models with low precision are likely to classify low risk borrowers as high risk, and models with low recall are likely to classify high risk borrowers as low risk. This would be problematic as it would result in a higher likelihood that borrowers will default on their loans.
