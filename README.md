# FakeNewsPrediction
Fake News PRecition using Machine Learning (NLP)


OVERALL APPROACH

The training data comprises of 20800 rows with 5 columns namely id, title, author, text and labels. The test data consists of 5200 rows and 4 columns. labels.csv consists of labels for the test data.

The implementation consists of 4 stages:
1. Loading the data into pandas dataframes
2. Preprocessing
3. Splitting into the training and testing set
4. Application of machine learning and deep learning models. In our assignment, we have implemented 4 classical ML models namely (Logistic Regression, Naive Bayes, Random Forest and XGBoost) and 1 deep learning model LSTM.

PRE-PROCESSING STEPS
The data is in the raw form and needs to be processed before it is used in a machine learning model. This involves the following steps:

1. Checking for Null values. In this data there were a considerable number of null values which we replaced with empty spaces.

2. For making the predictions, we used only the "author" and "title" columns due to the very large size of "text" column. The data from these 2 columns was merged into a single column called "Author&Title".

3. Stemming: This is a process of converting the words into their root form.

4. Checking for stopwords.
5. Lowercasing all the words to eliminate any capital letters and normalize the entire text.
6. Encoding: This is required to convert the text data into numbers. Here, we used one-hot encoding.

After that, we split the training data into train and test sets in the ratio 80:20

EVALUATION PROCEDURE AND METRICS

We applied 4 classical ML models namely ML models namely (Logistic Regression, Naive Bayes, Random Forest and XGBoost) and 1 deep learning model LSTM.

In all the cases, we printed the "Classification report" which included precision, recall and f1-score.

RESULTS

Accuracy was another metric that we checked by comparing the predicted value by actual value of the labels.

Among the 4 ML models, XGBoost gave the highest accuracy of 90.84%. The deep learning model LSTM gave the validation accuracy of 99.11%.

POSSIBLE IMPROVEMENTS
1. We can reduce the error on the test data which currently gives an error of 31% which is very high

2. The "text" column in the data can be merged with the data that we used for predictions. Eventhough the size of texts is very large, it will be a more complete implementation of this project

3. Different Deep learning models can be used such as transformers.

4. We can also tune the hyper parameters using grid search.
