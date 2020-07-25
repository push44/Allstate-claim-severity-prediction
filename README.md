# Allstate-claim-severity-prediction

readme template: https://github.com/sfbrigade/data-science-wg/blob/master/dswg_project_resources/Project-README-template.md

#### -- Project Status: [Completed]

## Project Intro/Objective
Allstate is an personal insurance company in the United States. The purpose of this project is to predict claims severity for the records of the test set. Though the train data set does not provide unit of the claims severity, values of the severity are continuous and hence this becomes a regression problem.

### Methods Used
* Exploratory data analysis
* Feature scaling
* Feature transformation
* Feature engineering
* Feature selection
* Predictive modelling
* Hyper-parameter tuning of machine learning algorithms
* etc.

### Technologies
* Python
* Pandas
* numpy
* jupyter
* sklearn
* etc. 

## Project Description
Data source for this project is available on the Kaggle website. The data set contains 130 feature columns and 188k rows. Of the 130 features 114 are categorical features and 16 are numerical features. The target feature a right skewed continuous feature. None of the features contain missing values which helps us to directly jump at the core of the project which feature transformation and feature engineering. Through exploratory data analysis we observe distributions of all of the features. Almost all numeric features exhibit some level of skewness and none of them look perfectly normal. On the other hand, out of 114 categorical features 72 features are binary and other are multi-level categorical with one feature containing maximum of just over 300 categories. In the EDA, pair plots and correlation matrix shows collinearity among the continuous features. The effect of collinearity is reduced by subtracting one numerical feature from another who shows more than 70% of collinearty amongs each other. Whereas, among the categorical features some of the features indicate high level of imbalanced distributions of feature categories. In feature engineering step, skewness of the numerical features is reduced by applying appropriate feature transformation to the features. For the categorical features, various features were engineered based on the simple statics such as mean, standard deviation, probability of occurances, etc. Hence, in-total 1464 number of features were present after feature engineering step. Using random forest regressor as an estimator recursive feature elimination with cross validation were performed to eliminate less effective features. This step reduced from 1464 number of features to just 264 features. In the next step which involved actully predicting target features. The preminary analysis of the machine learning algorithms done on the original 130 features revealed that ridge regression, random forest regressor, gradient boosting (xgboost), neural network models perform better than the other models on this data set. For each of the models hyperparameter were optimized as much as possible to the best of the current knowledge and time contraints. For neural network keras backend tensorflow framework was used. To find best neural network architecture keras tuner package was used.
