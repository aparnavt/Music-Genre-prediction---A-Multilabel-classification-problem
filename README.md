# Music-Genre-prediction---A-Multilabel-classification-problem

This project was done as part of a competition for participants of the Open Machine Learning Course by ODS in Dubai. This was hosted on Kaggle.

The goal is to predict musical genres of a track given some features extracted from the wave file and some metadata fields. One track can have several genres.

## Data Description

The data consisted of a train set consisting of features extracted from the music track. 

## Approach

Data pre-processing was applied to the data set and PCA was performed to reduce the dimensionality.

Since it was observed from the dataset, that genres are often related. There are parent genres and related genres. Hence identification of one genre , will help predict the remaining genres. To exploit this dependence, classifier chain was used for prediction. Prediction of a  genre was treated as a classification problem and result The result of one prediction was then 

https://www.kaggle.com/aparnavt/multiclass-classification
