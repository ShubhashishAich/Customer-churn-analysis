# Customer Churn Prediction
In today's fast-changing business world, being able to predict and prevent customers from leaving is crucial for keeping a healthy customer base and ensuring business growth. This project focuses on using different types of classification models, which are advanced tools for analyzing data, to foresee customer churn. By doing this, businesses can gather important insights to help them take early action and keep their customers happy and loyal.

Why Churn Analysis Matters?

- Proactive Decision-Making: Predicting customer churn empowers businesses to take proactive measures, addressing issues, implementing targeted marketing strategies, and tailoring customer experiences to retain valuable clients.

- Resource Optimization: Identifying potential churners allows businesses to optimize resources, focusing efforts and resources on customers who are more likely to stay.

- Continuous Improvement: Regularly updating and refining the model based on new data and insights ensures continuous improvement in prediction accuracy.




## Project Organization
```
.
├── Data/
    └── TelcoCustomerChurn                 : csv file
├── Images/                                : contains images
├── Customer Churn Prediction Model.ipynb  : Model Building for predicting customer churn
├── Exploratory Data Analysis.ipynb        : Data Analysis to understand customer data
├── LICENSE.md                             : MIT License
├── README.md                              : Report
└── model.pkl                              : Logisti Regression model
```
## Problem Objective
In this project, my goal is to conduct a customer churn analysis and develop a predictive model. The focus is on understanding the factors influencing customer attrition and leveraging advanced analytics to predict potential churners. The analysis involves examining customer behavior, identifying key indicators, and implementing classification algorithms for effective predictions.

## Dataset:
The Customer Churn table contains information on all 7,043 customers from a Telecommunications company in California in Q2 2022.
<br/>
 [Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn/data)

 ### The data set includes information about:

- Churn Information:

   The dataset includes a column named "Churn" indicating customers who have left within the last month.
- Services Data:

   Information on the services each customer has enrolled in, encompassing phone services, multiple lines, internet, online security, online backup, device 
   protection, tech support, and streaming TV and movies.

- Customer Account Information:

   Details about customer accounts, such as the duration of their subscription, contract type, payment method, preference for paperless billing, monthly charges, 
   and total charges.

- Demographic Information:

  Demographic details about customers, including gender, age range, and whether they have partners and dependents.
  This dataset provides a comprehensive overview of customer behavior, service usage, account specifics, and demographic characteristics, offering valuable 
  insights for analyzing and predicting customer churn.

## Implementation:

**Libraries:** sklearn, Matplotlib, pandas, seaborn, and NumPy

## Analysis
**Churn and Tenure Relationship:**

<p align="center">
<img src=https://github.com/ShubhashishAich/Customer-churn-analysis/blob/main/Images/Count%20of%20Each%20Tenure%20Period.png width="600" height="300"/>
</p>

- As we can see the higher the tenure, the lesser the churn rate. This tells us that the customer becomes loyal with the tenure.

<br />

**Churn and Contract Relationship:**

<p align="center">
<img src=https://github.com/ShubhashishAich/Customer-churn-analysis/blob/main/Images/Contract%20Vs.%20Churn.png width="340" height="250"/>
</p>

- The month-to-month contract exhibits a high churn rate, while the churn rate decreases with the increase in the contract period.

<br />


**PaperlessBilling By Contract Type:**

<p align="center">
<img src=https://github.com/ShubhashishAich/Customer-churn-analysis/blob/main/Images/Contract%20Vs.%20PaperlessBilling.png width="340" height="250"/>
</p>

- As we can see that the people with a month-to-month contract predominantly prefer PaperlessBilling.
<br />

<br />

**Payment method By Contract Type:**

<p align="center">
<img src=https://github.com/ShubhashishAich/Customer-churn-analysis/blob/main/Images/Contract%20Vs.%20PaymentMethod.png width="500" height="250"/>
</p>

- People having month-to-month contract prefer paying by Electronic Check mostly or mailed check. The reason might be short subscription cancellation process compared to automatic payment.

<br />

**Monthly Charges:**

<p align="center">
<img src=https://github.com/ShubhashishAich/Customer-churn-analysis/blob/main/Images/MonthlyCharges%20Vs.%20Churn.png width="340" height="250"/>
</p>

- As we can see the customers paying high monthly fees churn more.

<br />

## Modelling

In the modeling phase of the project, various machine learning models, including RandomForest and Ridge Classifier, were utilized to select the most effective model for predicting customer churn. The models were trained on 70% of the available data, and their performance was validated on the remaining 30%, meticulously avoiding any data leakage issues.

To fine-tune these models and optimize their performance, Grid Search Cross Validation was employed. This iterative process allowed for the systematic exploration of hyperparameter combinations, ensuring that the models were tuned to achieve optimal results without the risk of overfitting. A balanced approach was maintained to generalize well to new, unseen data.

<p align="center">
<img src=https://github.com/ShubhashishAich/Customer-churn-analysis/blob/main/Images/Confusion%20Matrix.png width="340" height="250"/>
<br />
<img src=https://github.com/ShubhashishAich/Customer-churn-analysis/blob/main/Images/Roc%20Curve.png width="600" height="400"/>
<br />
<img src =https://github.com/ShubhashishAich/Customer-churn-analysis/blob/main/Images/Cross-validated%20Model%20metrics.png width="600" height="400"/>
</p>
<br />
The final model resulted in 0.59 F1 score and 0.85 ROC-AUC.
<p align="center">
<br />
<img src=https://github.com/ShubhashishAich/Customer-churn-analysis/blob/main/Images/Feature%20Importance.png width="600" height="400"/>
<br />
</p>
From the feature importance plot, we can see which features govern the customer churn.
<br />
