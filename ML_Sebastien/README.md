## Machine Learning Part (Classification) :

### Introduction :

ML_Classifier_Sebastien.ipynb notebook is used to make the model and export it as a xgbmodel.bin file, this file can then be used for deployment by the Data Engineer.

### Data cleaning and preprocessing :

A quick EDA was performed on the data, there was no missing values which was a very good starting point.

Then, the features importances was computed on a separated notebook and 11 numerical features were selected to train the model.

These numerical features have some relationship with the categorical values, and thus, the categorical values wasn't selected for final modeling for keeping fitting time as fast as possible.

The two most important features was the total count of transaction, and the total amount transfered by these transactions, which basically give good information about the usage of the card, and thus the likelyhood of a customer to churn...

### Classification model :

The XGBoost classifier was used for this part, it was finetuned with the previously selected features of the dataset to optimise F1 Score to have a good balanced classifying score.

F1 Score is the harmonic mean of precision and recall. Precision measures the percentage of correctly predicted positive samples among all predicted positive samples, while recall measures the percentage of correctly predicted positive samples among all actual positive samples.

Therefore, F1 score is a way of summarizing a model's overall performance in terms of correctly identifying positive samples while minimizing false positives and false negatives.

### Dealing with the imbalance of the dataset :

There was an imbalance in the dataset in the Attrition Flag target, the classes are not equally represented, and the minority class (the attrited customer class) has significantly fewer examples than the majority class (the existing customer class). This can cause the model to be biased towards the majority class and perform poorly on the minority class, we try various techniques involving resampling (upsampling), with RandomOverSampler and SMOTE, and finally we try to adjust the `scale_pos_weight` of XGBoost. 

After various tests, this last method was finally selected.

### Further explanation about "scale_pos_weight" :

In XGBoost, `scale_pos_weight` is a hyperparameter that is used to balance the training of the model for imbalanced classification problems.

The `scale_pos_weight` parameter allows the user to adjust the balance between the positive and negative classes during training by assigning a weight to the positive class. This weight is used to increase the contribution of the positive class to the loss function during training. The higher the weight, the more importance is given to the positive class, and the better the model will be at predicting it.

In this case, as there was around 16% of churning customer in the dataset, we set the `scale_pos_weight` to the ratio of the number of negative samples to the number of positive samples, which in this case is 84/16 = 5.25. This will increase the weight of the positive class by a factor of 5.25, making it more important during training.

In summary, `scale_pos_weight` is a hyperparameter that is used to balance the classes during training for imbalanced classification problems by assigning a weight to the positive class.

### Model tree export :

To be able to simply explain how the model is working, we decided to use dtreeviz to export one of the model tree as an example.


![dtreeviz_tree.svg](./visuals/xgb_dtreeviz_tree.svg)
