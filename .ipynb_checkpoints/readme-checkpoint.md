# Syriatel Telecommunication Churn Prediction Analysis
## Project Overview
This project aims to use machine learning algorithms to predict customer churn for Syriatel Telecommunications. A comprehensive analysis is conducted, following the necessary machine learning processes to accurately predict customer churn and offer actionable recommendations.
## Business Understanding
SyriaTel, a leading telecommunications company, urgently needs to address customer churn, as the company has been losing a significant amount of revenue due to customers who do not return. A robust classifier is needed to predict customer attrition. The aim of this study is to utilize predictive machine learning analytics to identify patterns within SyriaTel's telecommunications data. Specifically, a binary classification model is required since the target variable is binary. This project seeks to provide SyriaTel with a predictive model that can identify customers at risk of churning in the near future and assist the telecom giant in reducing revenue loss by taking proactive steps toward customer retention and  long-term business sustainability.
### Research Questions
1. How do different machine learning predictive models differ in accuracy and specifity in Syriatel communication data.
2. What are the important features in predicting customer churn in the data.
3. What is the effect of data preprocessing techniques on predicting model accuracy.
### Study Objectives
1. To develop the best machine learning model for predicting customer churn.
2. To identify important features in predicting churn among customers.  
3. To evaluate the effect of various data preprocessing techniques on the target outcome.  
## Data Understanding
The project utilizes a dataset derived from Kaggle, which comprises Syriatel Telecommunication data. The dataset has 21 features and 3333 customer records, the features include billing records, demographic information and client contact details.

There are 4 object-type columns: 'state', 'international plan', 'phone number', and 'voice mail plan'. The remaining columns are numeric, consisting of both floats and integers.

Categorical columns :'international plan', 'voice mail plan'

Numerical columns :'number vmail messages', 'total day minutes', 'total day calls','total eve minutes', 'total eve calls','total night minutes', 'total night calls',  'total intl minutes', 'total intl calls', 'customer service calls','total charge'
              
       
The target variable is the 'Churn' column, which is categorical with 'yes' and 'no' responses.

Three columns—'state', 'account length', and 'phone number'—were dropped because they were not relevant to this study.

The dataset has no missing values or duplicate rows.

To identify the most important features, a new 'total charge' column was created by aggregating 'total day charge', 'total eve charge', 'total night charge', and 'total intl charge'into a single column.
## Data Preprocessing
The data was preprocessed to prepare it for modelling. The preprocessing involved;

  Three visualizations were created: a histogram, a pie chart distrinution for the target variable, and a correlation heatmap.

  The heatmap correlation waas used to identify the most correlated features with the target variable

  One Hot Encoding the categorical features; 'International plan' and 'voice mail plan'.

  Label Encoder for the target variable.

  Standard scaller for Numerical Features fron scikit learn Library

  Train test Split for splitting data into training and testing sets.
## Modelling 
The project employed two machine learning algorithms to predict customer churn, this includes;
  1. Logistic Regression
  2. Decision Tree Classifier.
### Logistic Regression Classification matrix After Cross Validation
  {'ROC-AUC For Train Data': 0.7694833625218914,
 'ROC-AUC For Test Data': 0.7451282230696566,
 'Accuracy Train': 0.7694833625218914,
 'Accuracy Test': 0.767616191904048,
 'confusion_matrix_train': <sklearn.metrics._plot.confusion_matrix.ConfusionMatrixDisplay at 0x1fc9915a1a0>}

  

### Decision Tree Classifier Classification Matrix After Cross validation
{'ROC-AUC For Train Data': 1.0,
 'ROC-AUC For Test Data': 0.8980075569394395,
 'Accuracy Train': 1.0,
 'Accuracy Test': 0.9235382308845578,
 'confusion_matrix_train': <sklearn.metrics._plot.confusion_matrix.ConfusionMatrixDisplay at 0x1fc98ed8730>}

### Decision Tuning Classification Matrix
{'ROC-AUC For Train Data': 0.9883975481611209,
 'ROC-AUC For Test Data': 0.8660042682713501,
 'Accuracy Train': 0.9883975481611208,
 'Accuracy Test': 0.9175412293853074,
 'confusion_matrix_train': <sklearn.metrics._plot.confusion_matrix.ConfusionMatrixDisplay at 0x1fc95c33af0>}
## Model Evaluation
### ROC_AUC to Select The Best Model
The AUC Analysis yield significant details about the classifier employed.
Based on the observation above , the decision tree has an AUC of O.86 indicating a respectable performance. It also depicts a false positive of 34 and 21 false negatives.  

The logistic regression on the other hand has an AUC of 0.82, falling slightly lower than the decision tree classifier. It however has a higher number of 126 false positives and 29 false negatives.

Based on these results, the decision tree classifier is a more better model for the sytiatel comuunication ltd. The decision tree boost of a slightly higher area under the curve, showcasing its superiority in distinguishing positive and negative classes.
## Conclusion
1. Decision tree classifiert after hyper parameter optimization is the best model strategy for syriatel communication ltd.It has the highest accuracy and AUC score, significantly outperforming logistic regression.
2. The analysis shows that 'total charges', in particular the aggregate sum of totl day charge, total evening charge,total night charge and total international charge is the most important feature in syriatel.
3. Effective data preprocessing, such as using SMOTE to address class imbalance and encoding categorical variables, is crucial for improving model performance. This highlights the significance of thorough data preparation in predictive analytics.



