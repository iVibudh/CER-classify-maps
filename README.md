## Overview 
In this section, we will be training models to classify pages from regulatory documents into maps (aka alignment sheet) or not maps. The Machine Learning models used for this task are XG Boost Classifier, Support Vector Classifier, Decision Treen Classifier,  Random Forest Classifier, Random Forest Regressor and XG Boost Regressor. The results from the regressor models are converted into binary output for the classification task, hence, I will be referring to these regression models as classification models. We will be comparing the accuracy and performance of the confusion matrix for these models on Test Set and Training Set. Then we will save the best performing model for future use. 

Description of the folder structure:
1. Training Set: This folder contains the files which are used to prepare the training set and the test set. 

2. Validation Set: This folder contains the files which are used to validate the trained models and then identify the best performing model. 

3. feature_extraction.py: This file contains the funtions which are used to extract the features in a PDF page. The features which are used to do the classification are: ...

4. Classify Maps.ipynb: In this file first we read the PDF files in the Training Set fonder. We treat each page as a unique entity and then we use functions from feature_extraction.py to extract feaures for all the pages. Then all these pages with their features are split in to Training set and Test Set. Then we train the classification models and evaluate the model performances. Further we exctract the features for the PDF in the Validation Set folder in the same way. Then we evaluate the models and pick the best model. 