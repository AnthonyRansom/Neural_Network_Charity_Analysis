# Neural_Network_Charity_Analysis
 
## Overview of Project

### Purpose

This analsyis will look creating a Machine Learning model that will me able to predict the succellfulness of charity applications from Alphabet Soup.

The model will use hiostorical data provided in order to train the model and determine the accuracy of the prediction the model makes.

## Results

### Data Preprocessing

Before the model is created the provided data was preprocessed
the following was determined from the data
 - The target variable is the "IS_SUCCESSFUL" column
 - The features variables are the "APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION", "INCOME_AMT", "SPECIAL_CONSIDERATIONS", "ASK_AMT" columns
 - The variable that are not considered targets or features are the "EIN","NAME","STATUS" columns

### Compiling, Training, and Evaluating the Model

The machine learning model was created and various changes were made to the model and data in order to achieve the required accuracy of 75% or more.
The tuning of the model did not meet the 75% accuracy but was able ti improve the accuracy to above 73.32% compared to the orignal model that achieved 72.59%. THe following details what was attempted to increase the accuracy
 - The model used that achieved a higher accuracy mase use of 3 layers with 150,100 and 50 neurons for each layer respectively along with using the activations function relu for the first 2 layers and then sigmoid for the last layer and the output layer. The relu adn sigmoid activation functions were used as they both work with values starting from 0 which no data in the dataset were negative values.
 -  No, The target performance of 75% was not achieved
 - The following was attempted to increase the accuracy
	- Attempt 1: additonal preprocessing was done the data where the "STATUS" feature was removed and the "ASK"AMT" feature was divided into 2 buckets
	- Attempt 2: looked at increaseing/decreasing the number of Neurons,hidden layers and epochs to various values
	- Attempt 3: looked at changing the activation functions for each hiden layer

## Summary

After that various attempts to increase the accuracy of the of the model the model that produced the highest accuracy of 73.32% was saved. The attampts to increase the accuracy was not able to achied the 75% minimum whihc may be due to insuffecient amount of data for the model to learn from or the provided features within the dataset do not provide enough data to the model accuractly make predictions.

Based on the dataset provided and the type of data a neural network may not be the best model to use and would recommend the use of a random forest supervised learning model. Random forest model are more robust to outliers in the data which the provided dataset as some large outliers within the "ASK_AMT" feature and are very good at ranking the importance of the input features.