## Hospital Readmission

This Jupyter Notebook implements model stacking, a Machine Learning ensemble technique, to predict hospital readmission risk for patients with diabetes. It includes data pre-processing for various data types such as numbers, categories, and text, utilizes multiple models, applies cross-validation to find optimal hyperparameters, and incorporates out-of-fold predictions. 

### Dataset:
* 8,000 training dataset
  * 40 columns  
  * 60% of person not being readmitted and 40% of person being readmitted 

### Preprocessing
* Apply Frequency and Ordinal Encoding for categorical data
* Apply StandardScaler for numerical data
* For text data, apply
  * Remove stopwords
  * Lemmatization
  * Text Frequency - Inverse Document Frequency (TF-IDF)

### Models
#### Base models
  * Logistic Regression for text data 
  * Support Vector Machine 
  * Random Forest
#### Meta model
  * Gradient Boosting Classifier

### Feature importance
![feature-importance](https://github.com/TienNguyen93/hospital-readmission/assets/43976085/a59fdd3d-eb52-4fa9-974e-75a8b9c747ef)

### AUC performance
AUC (Area Under the Curve) score represents the model's ability to discriminate between patients who will be readmitted and those who will not.

Why AUC? Because it allows hospitals to:
* Implement targeted interventions for high-risk patients to prevent readmission.
* Allocate resources more effectively.
* Improve patient outcomes.

An AUC score of **0.68** indicates that the model can effectively differentiate between the two groups (readmission vs. no readmission). 

![auc-score](https://github.com/TienNguyen93/hospital-readmission/assets/43976085/b2745032-208f-49fd-a119-b087b1cbc019)






