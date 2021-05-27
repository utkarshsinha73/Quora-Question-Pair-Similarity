# Quora-Question-Pair-Similarity
Program to check whether question similar to given one has been already added or not. This will save time of users as they won't have to answer similar questions again. 

1.EDA
The class distribution was found to be imbalanced with most question pairs in the dataset being duplicate. (Class Label 0)
Hence, log-loss taken as performance metric of the model.

2.Preprcessing
Some basic features like common word count, common word share etc. were extracted before text preprocessing.
Stemming and stopword removal was performed on the text to clean it. 
Subsequently some advanced features were extracted using fuzzy string matching. 

3.Featurization
TFIDF weighted Word2Vec was created from the cleaned text data and added to existing features.

4.ML Models
Random model was used as a baseline, giving a log-loss of 0.89.
Logistic Regression, SVC Classifier and XGBoost models were trained on the data. 
Best test log-loss was attained using XGBoost model: 0.34.
