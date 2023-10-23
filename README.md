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
- Start with a RandomForestClassifier, GradientBoostingClassifier, K Neighbors Classifier and Logistic Regression
- Evaluate which model works best and determine the most important features to be able to give practical recommendations.
  ### Modeling
  Using the above models mentioned we come to the conclusion that GradientBoostingClassifier is the best model to use as the accuracy test
![image](https://github.com/TULINYE/Churns_Telcom/assets/133999173/a44acfa3-abd6-4102-98dd-f93d38d1c856)
### EVALUATION
GradientBoostingClassifier is my best model so far. The combination of oversampling of the minority and undersampling of the majority has led to better results. The highest priority for my model is to have a good recall score. This model had the highest recall score which is why I'm taking this as my final model. The GradientBoostingClassifier model has performed well in predicting customer churn. The precision score for class 1 (churn) is 0.88, which means that when the model predicts a customer will churn, it is correct 88% of the time. The recall score for class 1 is 0.82, which means that the model correctly identifies 82% of all customers who actually churn. The F1-score for class 1 is 0.85, which is a harmonic mean of precision and recall and indicates the overall performance of the model for class 1. Additionally, the macro-average F1-score is 0.91, which means that the model performs well in both classes. The accuracy of the model on the test set is 0.96, which means that the model correctly predicts 96% of all customers' churn status
![image](https://github.com/TULINYE/Churns_Telcom/assets/133999173/8985a8f9-1e62-4175-bfa4-c47a0438e808)
![image](https://github.com/TULINYE/Churns_Telcom/assets/133999173/77c9f5df-b6c3-4096-a146-a0f6e4a98901)
According to the feature importance plot, the top three factors influencing the prediction of customer churn are total intl minutes, total night charge, and total night calls. This implies that customers with total intl minutes and total night charge are more inclined to churn. Additionally, customers who make night calls are also at a greater risk of churning.
### Summary & Recommendation
With the model, I have identified several factors that are important in determining the churn of the customer. While the model is not perfect, it will mostly catch those customers who are likely to leave. With this information, the telephone company can take steps to reduce churn and retain customers. They can target customer engagement by utilizing the "customer service calls" variable to identify customers who frequently contact customer service which may help improve their satisfaction and reduce the likelihood of churn, Customized retention Offerssuch as offering discounted international plans to customers who make frequent international calls and night calls, Offer quality of service improvements like network performance and call quality in areas where customers are most affected and Implement post-interaction customer surveys or feedback mechanisms, especially for customers with high "customer service calls" or those who have recently contacted customer support




