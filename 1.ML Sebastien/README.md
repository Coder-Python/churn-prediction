## Machine Learning Part (Classification) :

#### Introduction :

ML_Classifier_Sebastien.ipynb notebook is used to make the model and export it as a model.bin file, this file can then be used for deployment by the Data Engineer.

#### Data cleaning and preprocessing :

A quick EDA was performed on the data, there was no missing values which was a very good starting point.

Then, the features importances was computed on a separated notebook and 11 numerical features were selected to train the model.

These numerical features have some relationship with the categorical values, and thus, the categorical values wasn't selected for final modeling for keeping fitting time as fast as possible.

The two most important features was the total count of transaction, and the total amount transfered by these transactions, which basically give good information about the usage of the card, and thus the likelyhood of a customer to churn...

#### Resampling :

As there was an imbalance in the dataset in the Attrition Flag target, we use resampling to upsample the dataset to make it balanced, this improve the recall and thus F1 score.

#### Classification model :

The XGBoost classifier was used for this part, it was finetuned with the previously selected features of the dataset to optimise F1 Score to have a good balanced classifying score.




