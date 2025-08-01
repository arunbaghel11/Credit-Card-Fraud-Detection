Credit Card Fraud Detection
Project Overview
This project focuses on detecting fraudulent credit card transactions using a machine learning approach. The primary goal is to build and evaluate models that can accurately classify transactions as either genuine or fraudulent, with a specific focus on handling the challenge of class imbalance inherent in fraud detection datasets.

Dataset
The dataset used in this project is the creditcard.csv file, which contains transactions made by credit cards in September 2013 by European cardholders. This dataset presents a significant challenge due to its highly imbalanced nature, with fraudulent transactions making up only a small fraction of the total.

Source: Kaggle - Credit Card Fraud Detection

Methodology
The project follows a standard machine learning workflow, which includes:

Exploratory Data Analysis (EDA): Initial analysis to understand the dataset's structure, identify missing values, and visualize the class distribution.

Data Preprocessing: Standardizing the Amount feature using StandardScaler to ensure that all features contribute equally to the model's performance. The Time feature is dropped as it's not a strong predictive signal in this context.

Model Selection: Two popular ensemble models, Decision Tree Classifier and Random Forest Classifier, were chosen for their effectiveness in classification tasks.

Addressing Class Imbalance: The dataset's severe class imbalance is addressed using the Synthetic Minority Over-sampling Technique (SMOTE). This technique generates synthetic examples for the minority class (fraudulent transactions), balancing the dataset and improving the model's ability to detect fraud.

Model Evaluation: Models are evaluated using key metrics such as accuracy, precision, recall, and F1-score, with a particular emphasis on the confusion matrix to assess performance on both classes.

Results
After training and evaluation, the Random Forest Classifier with SMOTE oversampling was found to be the most effective model. It demonstrated superior performance in identifying fraudulent transactions, achieving a better balance between precision and recall compared to the models trained on the original, imbalanced dataset.

How to Run the Code
To run this project, you will need to have Python and the necessary libraries installed.

Prerequisites
You can install all the required libraries using pip with the requirements.txt file:

pip install -r requirements.txt

The requirements.txt file should contain:

numpy

pandas

matplotlib

scikit-learn

imbalanced-learn

Instructions
Download the creditcard.csv file from the Kaggle link.

Place the creditcard.csv file in the same directory as the Python script (credit_card_fraud_detection.py).

Run the Python script from your terminal:

python credit_card_fraud_detection.py
