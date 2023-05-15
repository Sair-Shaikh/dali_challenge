# dali_challenge
Data Challenge for DALI Lab Application

First, I explored each column of the Superstore data to find corelations, clusters, or trends. This work is in data_exploration.ipynb. I used seaborn for visualizations, and numpy and pandas for data manipulation. 

Then, I imputed the missing data using methods appropriate to each column (i.e. inferring for other columns, using the mean, or the mode, etc). Then, I converted the categorical data to numeric for each of analysis. Then I initialized a RandomForestRegressor to predict profits based on several variables. I used RandomizedSearchCV to perform hyperparameter tuning on 5 parameters (n_estimators, max_features, max_depth , and min_samples_split. After training, I used shap to explain and visualize the effect of each feature on the predictions. This work is in model1.ipynb.

Lastly, I took on the NLP challenge. I loaded the reviews, arranged them by size, and took randomized, evenly sized samples of the data to train on. Then, I trained a BertForSequenceClassification model on the data, setting up TrainingArguments as appropriate. After training, I created a pipeline for training and calculated a confusion_matrix to demonstrate accuracy. Then, I used shap to explain 3 subsets of the testing sentences:
the sentences BERT was most confident on, least confident on, and a random sample. The last part of this project was to visualize and explain how the model works, and what textual clues it picks on. This work is in nlp_challenge.ipynb.

