# Attrition-Data-Analysis-using-ML-Techniques-

##  Project Description
This project's goal is to make predictions about whether or not an employee would resign using certain parameters. Before applying machine learning algorithms, data was analysed, preprocessed, and feature engineering was carried out. On the basis of accuracy, precision, recall, F1 and ROC scores, various ML algorithms are contrasted. These measures are used to choose the final model, and grid search and stratified k-fold cross validation are used to tweak its hyperparameters.

## Data
Data is taken from IBM HR Analytics Employee Attrition & Performance at kaggle https://www.kaggle.com/pavansubhasht/ibm-hr-analytics-attrition-dataset/download
The downloaded file is present in Data folder. 

## Exploratory Data Analysis
1. To investigate the impact of characteristics on attrition, graphs of features vs. attrition are plotted.
2. A distribution analysis using a histogram of numerical features is performed.
3. The attrition distribution plot reveals extremely imbalanced data.**.

## Preprocessing and feature engineering
1. Categorical features are encoded using **one hot encoding scheme**.
2. Numerical features with **skewness** value greater than 0.8 are transformed using **log transformation.**
3. Three **new features** viz. tenure per job, years without change and compensation ratio were **created** using existing features.
4. **Irrelevant attributes** viz. EmployeeNumber, EmployeeCount, Over18 and StandardHours were **dropped**.
5. **One hot encoding** is used to transform cardinal categorical features.
6. **Label encoding** is used to transform ordinal categorical features and target labels.
7. Sybthetic Minority Oversampling Technique **SMOTE** is used to tackle data imbalance.
8. **Principal Component Analysis** is used for dimensionality reduction of data.

## ALgorithm tried
1. LogisticRegression
2. SVC
3. DecisionTreeClassifier 	    
4. RandomForestClassifier 	    
5. ExtraTreesClassifier 	      
6. GradientBoostingClassifier 	
7. AdaBoostClassifier 	        
8. GaussianNB 	

## Metrics used
Above models are compared on the basis of following metrics.
1. Accuracy
2. Precision
3. Sensitivity
4. F1
5. ROC

## Performance of various models
| Sr. No. |                      Model |  Accuracy | Precision | Sensitivity | Specificity | ROC Score |
|--------:|---------------------------:|----------:|----------:|------------:|------------:|----------:|
|    1    | LogisticRegression         | 77.966102 | 51.428571 | 66.666667   | 81.318681   | 0.739927  |
|    2    | SVC                        | 85.593220 | 75.000000 | 55.555556   | 94.505495   | 0.750305  |
|    3    | DecisionTreeClassifier     | 78.813559 | 54.545455 | 44.444444   | 89.010989   | 0.667277  |
|    4    | RandomForestClassifier     | 79.661017 | 63.636364 | 25.925926   | 95.604396   | 0.607652  |
|    5    | ExtraTreesClassifier       | 81.355932 | 77.777778 | 25.925926   | 97.802198   | 0.618641  |
|    6    | GradientBoostingClassifier | 83.898305 | 75.000000 | 44.444444   | 95.604396   | 0.700244  |
|    7    | AdaBoostClassifier         | 84.745763 | 73.684211 | 51.851852   | 94.505495   | 0.731787  |
|    8    | GaussianNB                 | 72.033898 | 43.478261 | 74.074074   | 71.428571   | 0.727513  |



Random forest can be employed as the ultimate model for predicting attrition, according to a comparison of models based on these metrics.
Following model completion, models were compared using "stratified k-fold cross validation" and "grid search" over a range of hyperparameters.
For the complete model, feature importance is plotted..

## Observations
1. Based on the importance of the features, it can be noted that our engineered features, such as "TenurePerJob," "CompRatioOverall," and "YearsWithoutChange," have greater importance values than many of the other features offered. Therefore, feature engineering was successful, it may be said.
2. SMOTE oversampling improved the accuracy of the model's predictions. Following the use of SMOTE, earlier models that were skewed towards forecasting the majority class alone no longer exist.
