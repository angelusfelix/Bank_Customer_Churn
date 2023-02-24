Download data = https://www.kaggle.com/datasets/gauravtopre/bank-customer-churn-dataset?resource=download
This dataset is talk about customer who will churn or not .
Problem Statement = Whats make customer churn?
Goal = Keep the customer from churning
Objective = Make model machine learning to get characteristic customer who will churn and give some recommendation
Metrics Model = Churn rate

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