
## Final project for the Machine Learning/ Ai fundamentals path on Codecademy

## Topic: Student Performance
Can final student performance (G3) be predicted from demographic, social, and school-related factors without using earlier grade indicators?
## Project Scoping
### Goal
The goal of the project is to investigate whether the final student performance, can be calculated based on the other variables in the dataset. The variables for student performance at g1 and g2 have high correlation with the final g3 performance metric, so ideally, I would like to predict g3 without g1 and g2.
### Data Gathering
I have a dataset from two Portuguese schools, with various variables, and I want to use this data to see whether it can predict the variable g3 which is the final grade metric.
### Analysis
The analysis will be done by removing the variables g1, g2 and g3, and using the rest as features for a ml model. I will then extract g3 to be the outcome variable. A train test split will then be done, then a scaler will be fitted on the training data and used to transform both the test and training data. I will then see whether the regression model trained on the training data performs well on the test data. Performance metrics will be r2 and error metrics on the test set.

## Conclusions
I made an ML Pipeline and compared the Ridge regression and Random Forest models. The random forest model performed better and explained 27% of the variance.
Various models were trained and tested. The Random Forest model was best at predicting student grades when G1 and G2 were excluded, explaining approximately 27% of the variation in final grade (R² ≈ 0.27). The Ridge Regression model performed worse, with an R² of 0.10, indicating limited linear predictive power.
The Random Forest model achieved an RMSE of about 3.87, meaning predictions typically deviate by roughly 3.9 grade points on the 0–20 scale. Given the exclusion of prior grades (which are strong predictors), this error rate is reasonable and indicates moderate predictive capability.
The superior performance of Random Forest compared to Ridge Regression suggests the presence of nonlinear relationships between features and student performance.
<img width="330" height="217" alt="image" src="https://github.com/user-attachments/assets/19f6a25d-3c48-4431-b2d5-f00617fb8473" />
The most important predictor was number of absences, suggesting that absence from classes has the strongest relationship with grades of the included variables.


