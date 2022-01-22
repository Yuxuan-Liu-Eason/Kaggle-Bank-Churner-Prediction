# Kaggle-Bank-Churner-Prediction
https://www.kaggle.com/sakshigoyal7/credit-card-customers

The aim is to predict who will leave the bank’s credit card services and to decide what aspects to improve to prevent churning based on customers’ demographic and account related information. The customer churn rate reflects the quality of products and the ability to retain users.

## EDA
- Attrition_Flag is negatively correlated with Total_Trans_Ct and Total_Revolving_Bal, etc. They are all potentially significant features.
- Avg_Open_To_Buy is highly correlated with Credit_Limit. Maybe drop one of them later.
- Credit_Limit, Avg_Open_To_Buy are highly right-skewed. Maybe apply transformation later.

## Feature Enigneering
- Use KNN to fill the unknowns in Education_Level, Marital_Status and Income_Category.
- Added 6 new features based on existing features.
- Use Box-cox transformation to improve the shape of Total_Trans_Amt, Credit_Limit, Avg_Open_To_Buy.
- One-hot encoding.
- Try PCA for dimension reduction

## Models
Use Logistic Regression, SVM, Random Forest, and LightGBM respectively and contrast their performance.
![image](https://user-images.githubusercontent.com/76148884/150622530-664db473-9721-486f-a992-77a4b344a398.png)
![image](https://user-images.githubusercontent.com/76148884/150622534-261020e1-edd2-41e9-b536-517e3f06597f.png)
LightGBM has the best performance.

The most important features are Total_Trans_Amt, Toal_Trans_Ct, Total_Amt_Chng_Q4_Q1, etc. We can conclude that the decrease of user activity is the sign of churning.
