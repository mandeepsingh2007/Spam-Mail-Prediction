# Spam Mail Classification

This project demonstrates the classification of spam and ham (non-spam) emails using machine learning techniques. The model is trained using a dataset of labeled emails, and it predicts whether an input email is spam or not.

## Libraries Used
- `numpy`: For numerical computations.
- `pandas`: For data manipulation and analysis.
- `sklearn`: For machine learning tasks.
  - `train_test_split`: To split the dataset into training and testing sets.
  - `TfidfVectorizer`: For feature extraction from text data.
  - `LogisticRegression`: For training the classification model.
  - `LabelEncoder`: For encoding categorical labels.
  - `accuracy_score`: For evaluating the model's performance.

## Dataset
The dataset consists of emails categorized as either spam or ham. The `mail_data.csv` file contains the following columns:
- `Message`: The text of the email.
- `Category`: The category of the email (either `spam` or `ham`).

## Model
The project uses a **Logistic Regression** model to classify emails into two categories:
- **Spam (1)**
- **Ham (0)**

## Steps:
1. **Preprocessing the Data**:
   - The `Category` column is encoded into numerical values using `LabelEncoder`. 
   - The `Message` column is used as input data (X) and `Category` as output data (Y).
   
2. **Feature Extraction**:
   - The `TfidfVectorizer` is used to convert the email messages into numerical features that the model can understand. Stop words are removed and the text is converted to lowercase.

3. **Model Training**:
   - The dataset is split into training and testing sets using `train_test_split`.
   - A Logistic Regression model is trained on the training data.

4. **Model Evaluation**:
   - The accuracy of the model is calculated on both the training and testing data.

5. **Prediction**:
   - A sample input email is classified as either **spam** or **ham** based on the trained model.

## Accuracy:
- **Accuracy on Training Data**: 96.76%
- **Accuracy on Testing Data**: 96.68%

## Example Prediction
For an input email:

> _"Congratulations! You've been selected to win a $1,000 gift card. Reply YES to claim your prize. Hurry, offer expires soon!"_

The model predicts whether it is a **Spam Mail** or **Ham Mail**.


## Conclusion
This project demonstrates the effectiveness of text classification using machine learning techniques. The high accuracy indicates that the Logistic Regression model is suitable for the task of spam detection.
