# **Telecom Customer Churn Prediction**

![1684875715973](image/README/1684875715973.png)

## Overview

Customer churn refers to the phenomenon where customers cease their relationship with a company or discontinue using its products or services. Predicting customer churn is crucial as it allows companies to identify customers who are likely to leave and take proactive measures to retain them. This is important because losing customers results in revenue loss, reduced market share, and increased costs of acquiring new customers. Additionally, customer churn can negatively impact a company's reputation and disrupt its growth plans. By predicting and addressing churn, businesses can improve customer retention, enhance profitability, and maintain a competitive edge in the market.

## 1.Business Understanding

Maven Communications, a telecommunications company, wants to create a model  that can predict if customers will stop using their services soon. This is important because Maven Communications wants to reduce the amount of money they lose when customers leave. They want to know if there are any patterns that can help them predict when customers might leave., and it will help them identify customers who are likely to stop using their services. This information will help Maven Communications take action to keep those customers from leaving.

### Problem Statement

As a BI Consultant, my role is to assist Maven Communications in predicting customer's  churn and reducing revenue loss by analyzing customer data and identifying patterns, I will develop a classification model to predict if a customer will churn or not. This model will leverage customer details, service usage, and other relevant information. The insights derived from the analysis will drive strategies to enhance customer experience, optimize resource allocation, and increase customer loyalty. Through this project, my objective is to contribute to Maven Communications' goal of improving customer retention, financial performance, and market competitiveness.

### Specific Objectives

* To build a classification model which can predict if a customer will churn or not.
* To find out how to optimize customers retention and increase Customer Satisfaction
* To Analyse the data in terms of various features responsible for customer Churn
* To understand customers pain point (Issues that customer experience that make them churn)

### Success Metrics

The metrics we will use to measure the success of this model are as follows:

* Achieving an accuracy score of over 85 percent.
* Achieving a recall rate of over 60 percent. It is more favorable to correctly identify a customer as churned even if they haven't, rather than incorrectly predicting that they haven't churned when they actually have. The latter scenario can lead to significant losses and is considered worse.

## 2.Data Understanding

### Overview

 A full description of all the features in the DataFrame can be found [here]([https://www.kaggle.com/datasets/shilongzhuang/telecom-customer-churn-by-maven-analytics](https://www.kaggle.com/datasets/shilongzhuang/telecom-customer-churn-by-maven-analytics)).

### Data Description

* This data has 38 columns and 7043 rows.
* Each row represents a unique customer   and each column gives metadata about the customer.
* This data pertains to the customers that the companies have  had during the second quarter of 2022 Q2, collected over a three-month period from April 1st to June 30th.

## 3.Data Preparation

The Steps involved are:

* Detecting and dealing with missing values.
* Dealing with duplicates
* Conversion of columns to their correct data types and checking for inconsistencies
* Dealing with outliers.

### Data Cleaning

The dataset had missing values in several columns, including the churn category and churn reason column. Filling the missing values in these columns could affect the data distribution. Additionally, other columns, such as internet service, online security, and streaming TV, had missing data. These columns were filled using forward fill. Some data was also missing in the columns for average monthly long distance charges and multiple lines. Finally, the "Id" column was dropped as it was not relevant for the prediction model.No duplicates were found or data inconsistencies.

## 4.Modelling

In the analysis, a logistic regression model was fitted as the vanilla model, and its performance metrics were evaluated. Three additional classification models were also fitted, and their performance metrics were assessed. The two best-performing models were selected based on accuracy and recall(Logistic Regression and Random Forest). The remaining models underwent tuning processes to address class imbalance, apply ensemble methods, and analyze feature importance. After the tuning process, the best-performing model was chosen for predicting customer churn. The models used in this analysis included logistic regression, K Nearest Neighbors (KNN), decision trees, and random forest.

## 5.Final Model Evaluation

After thorough evaluation, the Gradient Boosted Tree emerges as the optimal choice for our final model. It showcases exceptional accuracy, achieving training and test scores of 0.89 and 0.87, respectively. Maven Communication will utilize this powerful model to accurately predict customer churn, allowing proactive measures to be implemented and mitigating potential revenue loss. Notably, the model demonstrates a recall score of 70 for class 0 (customer churning) and an impressive 95 for class 1, enabling Maven Communication to effectively identify customers at risk of churn and tailor retention strategies accordingly.

## 6.Conclusion

* Gradient boosted Trees is the best classifier to be used to predict if a given customer will churn or not.
* Los Angeles, San Diego and Sacramento location have the highest numbers of customers and the highest churn rate.
* Increase in charges either monthly or total charges make customer churn.
* Customers with zero dependants and the unmarried ones tend to churn more.
  *Majority of the customers don't recieve offers and tend to churn more.
* Most of the customers did not have premium subscription like online backup, online security, Device protection plan or premium tech support and they churned more.
* Most customers did not recieve referrals and those with no referral churned more.

## 7.Recommendation

1. Use Gradient Boosted Trees: Employ this classifier for accurate customer churn prediction.
2. Monitor and Address Pricing: Be cautious of increasing charges as it may lead to customer churn.
3. Offer Incentives: Provide attractive offers to customers as those without offers are prone to churn.
4. Enhance Premium Subscriptions: Promote premium features like online backup, online security, device protection plan, and premium tech support to reduce churn.
