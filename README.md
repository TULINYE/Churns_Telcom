# Churns_Telcom
![churn](https://github.com/Julez89/dsc-phase-3-project-v2-3/blob/main/images/churn.png)
### OVERVIEW 
In this study, I analyzed the 'SyriaTel Customer Churn' data. The SyriaTel is a telecommunication company. The purpose of the study is to predict whether a customer will ("soon") stop doing business with SyriaTel.
### BUSINESS PROBLEM
A telecommunications company based in the United States is seeking to reduce its customer attrition rate, which currently stands at 15%. This high churn rate is driving up marketing expenses as the company must continually acquire new customers. Presently, the company employs a random approach to offer discounts or incentives to certain customers without prior knowledge of their intent to leave or stay. Their objective is to proactively detect customers likely to churn and employ strategies to retain them, while avoiding unnecessary spending on customers who have no intention of leaving. Key questions that we aim to address include:

What are the primary customer characteristics that can effectively predict customer churn?
Can we accurately identify customers who are on the verge of leaving?
Is it possible to minimize the allocation of discounts or incentives to customers who have no intention of churning?
### DATA
### Scrub/Explore

The column/variable names are:
* state            
* account length
* area code
* phone number 
* international plan
* voice mail plan
* number vmail messages
* total day minutes
* total day calls
* total day charge
* total eve minutes
* total eve calls
* total eve charge
* total night minutes
* total night calls
* total night charge
* total intl minutes
* total intl calls
* total intl charge
* customer service calls
* churn
Regarding my target variable (churn), we are dealing with class imbalance. 85% of the data set contains information about staying customers and only 15% churn.
![image](https://github.com/TULINYE/Churns_Telcom/assets/133999173/0bd8f3b0-9973-40b9-b2e4-b7bd2c3c5e1f)
### Approach

This task is a classification problem because my target variable is a categorical variable. It is either yes or nor for a customer that churns.
I used a machine learning approach to solve the classification task. Machine learning algorithms are designed to automatically identify patterns and relationships within data, allowing them to detect complex relationships that may not be immediately apparent through manual analysis. Also, machine learning algorithms can improve over time as they are trained on more data, providing an ongoing opportunity to refine and improve the accuracy of the classification model. Finally, they are able to handle large amounts of data efficiently and quickly, making them an ideal choice for tasks involving large datasets. 
I am using an iterative approach to try to find the best model for my predictions.
In summary, I took the following steps:
- Loading and combining data
- Check for data completeness and overall structure
- Inspect all variables visually to determine relevance for future model
- Prepare data for modeling (one hot encoding, scaling, train - test split, resampling  )
- Start with a RandomForestClassifier, GradientBoostingClassifier, K Neighbors Classifier and logistic Regression
- Evaluate which model works best and determine the most important features to be able to give practical recommendations.
- 








