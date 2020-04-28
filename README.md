# Predicting House Sale Prices With Linear Regression & Cross Validation
In this project we predict house sale prices using housing data for the city of Ames, Iowa, United States from 2006 to 2010. 

* <a target="_blank" href="https://www.kaggle.com/samaxtech/ames-housing-data#AmesHousing.tsv">Download Data</a>
* <a target="_blank" href="https://s3.amazonaws.com/dq-content/307/data_description.txt">Columns Explanation</a>

<b>transform_features()</b> - Within this function we remove the non-numerical and other features that are not meaningful for our model. Besides that we remove all features that have more than 25% missing values. Finally we either delete the rows (for non continuous features) or replace the missing values for the mean()

<b>select_features()</b> - After identifying the features which are highly correlated, we remove those of the pairs, which have less impact on the model. Within this funciton we also re-scale the features and remove those with very low variance.
<b>train_and_test()</b> - Here we train and test our model with the remaining features. We perform the process by splitting the set in 50/50 (train/test) and also try different cross-validation combinations.

Results show that, for this dataset, increasing the number of datasets in the k-fold cross validation leads to always smaller RMSEs
