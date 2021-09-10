# Bank Marketing Campaign

The Main objective of this dataset's machine learning is to optimize the marketing camapign of banking instituion in the future.

**1. Initial Hypothesis and EDA**

Features on this Dataset :
- Age
- Job
- Marital Status
- Education
- Credit (Default)
- Balance
- Housing (Yes/No)
- Loan (Yes/No)
- Contact
- Day, Month
- Call Duration
- Campaign
- Number of Days passed after campaign
- Number of campaign performed
- Outcome
- Target Y (Yes/No)

Assume that Age, Job, Marital Status, Education, Credit, Balance, Housing, Loan, Contact, Call Duration, Campaign, Number of Days, Number of Campaigns will affect the Outcome of the Marketing Campaign.

The result after checking the Association between these features (Cramer's V Method)

![Association](https://github.com/tommysachi/Bank_Marketing_Campaign/blob/main/Table%20%26%20Visual/Association.JPG)

Dropping the Features that are below than 0.1.

**2. Machine Learning**
Because of the Imbalance Data, when performing data splitting, we used stratify=y.

Using 3 Base Models Algorithm :
- Logistic Regression
- KNN (K Nearest Neighbors)
- SVM (Super Vector Machine)

The Classification of the Base Models as shown below :

![Classification Report](https://github.com/tommysachi/Bank_Marketing_Campaign/blob/main/Table%20%26%20Visual/Classification%20Report%20Base%20Model.JPG)

Because of the Imbalance Data, we used SVM algorithm that has Class Weight Parameter to improvised the Model.

**3. Improvement**

- Tuning for the Best Class Weight Parameter.

    ![Class Weight](https://github.com/tommysachi/Bank_Marketing_Campaign/blob/main/Table%20%26%20Visual/Class%20Weight%20Imbalance.JPG)

    The Confusion Matrix and Classification Report of this Improvement as shown below :

    ![CM CR Class Weight](https://github.com/tommysachi/Bank_Marketing_Campaign/blob/main/Table%20%26%20Visual/CM%20and%20CR%20Class%20Weight%20SVM%20Model.JPG)

    This Model has shown better Evaluation Matrix.

- Scaling the Balance Feature (Continuous Data) with Robust Scaler.

    The Confusion Matrix and Classification Report of this Improvement as shown below :

    ![CM CR Scaling](https://github.com/tommysachi/Bank_Marketing_Campaign/blob/main/Table%20%26%20Visual/CM%20and%20CR%20Scaled%20SVM%20Model.JPG)

- Hyperparameter Tuning with Grid Search.

    The Confusion Matrix and Classification Report of this Improvement as shown below :

    ![CM CR Hyperparameter](https://github.com/tommysachi/Bank_Marketing_Campaign/blob/main/Table%20%26%20Visual/CM%20and%20CR%20Hyperparameter%20SVM%20Model.JPG)

- Manual Tuning SVM (C Value).

    ![Manual Tuning](https://github.com/tommysachi/Bank_Marketing_Campaign/blob/main/Table%20%26%20Visual/Manual%20Tuning%20C%20SVM.JPG)

    The Confusion Matrix and Classification Report of this Improvement as shown below :

    ![CM CR Manual Tuning](https://github.com/tommysachi/Bank_Marketing_Campaign/blob/main/Table%20%26%20Visual/CM%20and%20CR%20Manual%20Tuning%20SVM%20Model.JPG)

    This Model has shown better True Positive, with C value = 5.

- Summary Evaluation Matrix

    ![Summary](https://github.com/tommysachi/Bank_Marketing_Campaign/blob/main/Table%20%26%20Visual/Evaluation%20Matrix.JPG)

**4. Prediction**

![Prediction](https://github.com/tommysachi/Bank_Marketing_Campaign/blob/main/Table%20%26%20Visual/Prediction%20Model.JPG)

The Prediction Outcome of Success or Fail Marketing Campaign.



