# Music-Genre-prediction---A-Multilabel-classification-problem

This project was done as part of a competition for participants of the Open Machine Learning Course by ODS in Dubai. This was hosted on Kaggle.

The goal is to predict musical genres of a track given some features extracted from the wave file and some metadata fields. One track can have several genres.

## Data Description

The data consisted of a train set consisting of features extracted from the music track. 

## Approach

Data pre-processing was applied to the data set and PCA was performed to reduce the dimensionality.

It was observed from the dataset that the genres are often related. There are parent genres and related genres. Hence identification of one genre , will help predict the remaining genres. To exploit this dependence, classifier chain was used for prediction. Prediction of a  genre was treated as a classification problem and result of a prediction was used as input for the next classifier. The order of prediction (genres) was important in this case. The frequency of each genre in the train set was computed. Only the most frequent 38 genres (those which had more than 1000 samples ) were used for prediction. The classifiers were ordered in such a way that the first classifier predicted the least frequent among these 38, the second classifier for the second most frequent genre and so on. 

In the train set, the median number of genres was 4. So a genre was selected as true, for a certain prediction probabilty so that the median value for number of genres remained 4 in the test set as well. The most frequent 2 genres was added to genre list of all tracks. It was observed that hamming loss, accuracy, precision and f1 score all improved with this selection of values.


## Notebook

The code for this project is available at below link

https://www.kaggle.com/aparnavt/multiclass-classification


