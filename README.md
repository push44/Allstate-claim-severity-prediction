# Allstate-claim-severity-prediction

## Project Requirement:
Allstate is an personal insurance company in the United States. Predicting clients' claim severities are essential for insurance companies for their risk managements. This project is my first data science project where conduct several steps of the data science life cycle such EDA, Feature engineering, Feature selection, Machine learning models' performance analysis, etc.

## Files used in the project:
<ol>
  <li>EDA.ipynb</li>
  <li>feature-extraction.ipynb</li>
  <li>feature-selection.ipynb</li>
  <li>ML algo analysis.ipynb</li>
  <li>train-and-tune-on-selected-feat.ipynb</li>
</ol>

## Problem formulation and performance metric:
As the claims severity is a real valued feature this is a regression problem.

Mean Absolute Error (MAE): <img src="https://render.githubusercontent.com/render/math?math=\sum_i(|y_i - \hat{y_i}|)">

## Data Information:
<ul>
  <li>Total 130 predictor features</li>
  <li>Number of categorical features: 114
    <ul>
      <li>Number of binary features: 72</li>
      <li>Number of multi-variate features: 42</li>
    </ul>
  </li>
  <li>Number of numerical features: 16</li>
</ul>

## Key findings from EDA:

Pair plots and correlation matrix shows collinearity among the continuous features. The effect of collinearity is reduced by subtracting one numerical feature from another who shows more than 70% of collinearty amongs each other.

## Feature scaling:

Skewness of the numerical features are reduced by applying appropriate feature transformations.

## Feature Engineering:
For the categorical features, various features were engineered based on the simple statics such as mean, standard deviation, probability of occurances, etc. Hence, in-total 1464 number of features were present after feature engineering step.

## Feature Elemination:
Using random forest regressor as an estimator recursive feature elimination with cross validation were performed to eliminate less effective features. This step reduced from 1464 number of features to just 264 features.
