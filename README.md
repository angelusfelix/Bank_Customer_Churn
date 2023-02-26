Download data = https://www.kaggle.com/datasets/gauravtopre/bank-customer-churn-dataset?resource=download
1. This dataset is talk about customer who will churn or not .
2. Problem Statement = Whats make customer churn?
3. Goal = Keep the customer from churning
4. Objective = Make model machine learning to get characteristic customer who will churn and give some recommendation
5. Metrics Model = Churn rate

# EDA
1. Shape dataset = 10000 rows x 11 columns (10 features and 1 target).
2. Only feature credit_score and age have outliers.
3. Credit score, tenure, estimated salary are normal distributiom.
4. Age is positive distribution features.
5. Balance is bimodial. 
6. The customers who kept the most money at Bank AFS were customers from France, however, only 19% of the 4204 French customers survived from that country.
7. Customers with male gender are the customers who register the most at Bank AFS, but those who still survive (do not churn) are dominated by female customers.
8. There is no correlation among numerical feature.
9. The Scatterplot relates numerical features to one another. The insights obtained are that customers aged 40-70 years are customers who churn a lot, customers with a balance of USD 70,000 - USD 170,000 are also customers who are classified as churn a lot.

# Model Prediction
1. Split train test = 80% train 20 % test 
2. Feature Extraction = 0
3. Feature Transformation
- a. credit_score : Power Transformer
- b. balance : MinMax Scaler
- c. age : Power Transformer
- d. tenure : Robust Scaler
-  e. estimated_salary : Quantile Transform
4. Feature Encoding
- a. gender : Male 1, Female 0
-  b. country : France 2, Germany 1, Spain 1
5. Class Imbalance : Random Over Sampler
6. Using Recall, cause we need a small number of customer churn
7. Alghorithm: Recall Train and Recall Test : Condition
- a. Logistic Regression : 0.721 and 0.676 : Best fit 
- b. XGBoost : 0.721 and 0.679 : Best fit
- c. SVM : 0.719 and 0.666 : Best fit but computation takes longer than other algorithms
- d. Adaboost : 0.753 and 0.735 : Best fit
- e. Decision Tree : 1.00 and 0.482 : Overfit
- f. K-Nearest Neighbor : 0.748 and 0.684 : Best fit
- g. Random Forest Classifier : 1.00 and 0.487 : Overfit
- h. Naive Bayes : 0.734 and 0.732 : Best fit.
From 8 alghoritms that i have done, i choose naive bayes, cause the recall gap is smallest, and then the value of False Negative is smallest too
