# Project Title: Credit Risk Resampling

This project includes a Jupyter notebook that contains the following: a dataset of historical lending activity from a peer-to-peer lending services company, and a logistic regression model to compare two versions of the dataset that can identify the creditworthiness of borrowers.


Dataset:
---
lending_data.csv

Overview of the Analysis:
---

The purpose of this analysis is to train and evaluate machine learning models with imbalanced classes. This is due to the classification problem posed by credit risk that's inherently imbalanced. The imbalance is due to healthy loans easily outnumbering risky loans.

The data provided the following financial information to help predict the loan's risk:
* Loan Size (Amount)
* Interest Rate
* Borrower's Income
* Borrower's Debt/Income Ratio
* Borrower's Total Accounts
* Borrower's Derogatory Marks
* Borrower's Total Debt
* Loan Status (Healthy vs. High-Risk)

The data was separated into labels and features to allow the machine learning models to predict future loan statuses. The labels variable (y) was set to loan_status column. The features variable (X) was set to all the remaining columns excluding loan_status. In Model 1, the balance of the labels variable (y) using the value_counts function counted 75,036 (0's) and 2,500 (1's). 0 represents a healthy loan while 1 represents a high-risk loan. In Model 2, the balance of the labels variable (y) was 56,271 (0's) and 56,271 (1's).

The first stage of the machine learning process was to split the data into training and testing datasets by using train_test_split function of the train_test_learn module. The second stage was to fit a logistic regression model by using the training data (X_train and y_train). The third and final stage of the machine learning process was to save the predictions on the testing data labels by using the testing feature data (X_test) and the fitted model.

The methods for fitting the models were first using the LogisticRegression classifier on the original data. Next, the LogisticRegression classifier was used on resampled data by utilizing the RandomOverSampler module from the imbalanced-learn library. 

## Results
* Machine Learning Model 1 (Logistic Regression with Original Data):
    * Balanced Accuracy Score: 95.2%
    * Precision Score: 
        * 0 (healthy loan) - 100%
        * 1 (high-risk loan) - 85%
    * Recall Score:
        * 0 (healthy loan) - 99%
        * 1 (high-risk loan) - 91%    

* Machine Learning Model 2 (Logistic Regression with Resampled Data):
    * Balanced Accuracy Score: 99.4%
    * Precision Score: 
        * 0 (healthy loan) - 100%
        * 1 (high-risk loan) - 84%
    * Recall Score:
        * 0 (healthy loan) - 99%
        * 1 (high-risk loan) - 99% 

## Summary

The results of the machine learning models were both highly accurate with Model 2 outperforming Model 1 by 4.2%. Model 2 performs the best due to having the best balanced accuracy score and equal recall scores of 99%. Performance matters when trying to solve the creditworthiness of borrowers. Therefore, we recommend Model 2 which best predicts the loan status.

---

## Technologies: Python 3, Jupyter Notebook
---
Python 3 or later.

Jupyter Notebook for IDE.

---

## Usage:
---

Ensure the proper libraries and dependencies have been imported.

![image](https://user-images.githubusercontent.com/34729547/198850086-ac430401-0c32-442a-ae2b-1fffb9f8a3f8.png)


---

## Contributors: Nia Robinson

LinkedIn: https://www.linkedin.com/in/niaelanrobinson/

---

## License

MIT License.
