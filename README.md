<h1 align="center">Bank Term Deposit Analysis</h1>

The data is related with direct marketing campaigns of a Portuguese banking institution. The marketing campaigns were based on phone calls. Often, more than one contact to the same client was required, in order to access if the product (bank term deposit) was subscribed or not. 

Data set has 20 predictor variables (features) and around 41K rows.

# Data Defination
1. age (numeric)
2. job : type of job (categorical: 'admin.','blue-collar','entrepreneur','housemaid','management','retired','self-employed','services','student','technician','unemployed','unknown')
3. marital : marital status (categorical: 'divorced','married','single','unknown'; note: 'divorced' means divorced or widowed)
4. education (categorical: 'basic.4y','basic.6y','basic.9y','high.school','illiterate','professional.course','university.degree','unknown')
5. default: has credit in default? (categorical: 'no','yes','unknown')
6. housing: has housing loan? (categorical: 'no','yes','unknown')
7. loan: has personal loan? (categorical: 'no','yes','unknown')
8. contact: contact communication type (categorical: 'cellular','telephone')
9. month: last contact month of year (categorical: 'jan', 'feb', 'mar', …, 'nov', 'dec')
10. dayofweek: last contact day of the week (categorical: 'mon','tue','wed','thu','fri')
11. duration: last contact duration, in seconds (numeric). Important note: this attribute highly affects the output target (e.g., if duration=0 then y='no')
12. campaign: number of contacts performed during this campaign and for this client (numeric, includes last contact)
13. pdays: number of days that passed by after the client was last contacted from a previous campaign (numeric; 999 means client was not previously contacted)
14. previous: number of contacts performed before this campaign and for this client (numeric)
15. poutcome: outcome of the previous marketing campaign (categorical: 'failure','nonexistent','success')
16. emp.var.rate: employment variation rate - quarterly indicator (numeric)
17. cons.price.idx: consumer price index - monthly indicator (numeric)
18. cons.conf.idx: consumer confidence index - monthly indicator (numeric)
19. euribor3m: euribor 3 month rate - daily indicator (numeric)
20. nr.employed: number of employees - quarterly indicator (numeric)
21. y - has the client subscribed a term deposit? (binary: 'yes','no')

# Project Overview
In this analysis we perform:

1. Exploratory Data Analysis
2. Univariate Analysis
3. BiVariate Analysis
4. Model Fitting and Treating Imbalanced Data <br>

To treat the imbalance data so that there is no bias in modeling, we have used - 

1. RANDOM UNDRSAMPLING
2. RANDOM OVERSAMPLING
3. SYNTHETIC MINORITY OVERSAMPLING TECHNIQUE (SMOTE)

We have implemented the following Machine Learning Models - 

1. Logistic Regression Model
2. Decison Tree
3. Random Forest
4. Support Vector Machine


# Evaluation Metrics

For evaluating the models we have used Precision, Recall and Accuracy. <br>

| Model      | Data Type | Precision | Recall | Accuracy |
| ----------- | ----------- | ----------- | ----------- |
| Logistic Regression Model | Imbalanced Data | 0.68 | 0.42 | 90.88% |
| Logistic Regression Model | Undersampled Data | 0.45 | 0.88 | 86.13% |
| Logistic Regression Model | Oversampled Data | 0.42 | 0.87 | 85.63% |
| Decison Tree | Imbalanced Data |  0.62    | 0.55 | 91.42% |
| Decison Tree | SMOTE Data |  0.46    | 0.82 | 87.04% |
| Random Forest | Imbalanced Data | 0.26 |  0.75 | 73.88% |
| Random Forest | SMOTE Data | 0.31 |  0.69 | 79.67% |
| Support Vector Machine | SMOTE Data | 0.96 | 0.86 | 91.16% |



# Conclusion
For the given data, visualization of data, ways to treat imbalance in the data and best predictive model to determine the term deposit subscription was explored. From visualization, it can be derived that repeated campaign calls to customers within 20 days of previous call increases the subscription. After treating the imbalance in data, Decision Tree Model performed the best in terms of accuracy score of 91.42%.
