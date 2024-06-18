I opened the training features set and checked the columns and data .
I found some categorical columns i separated it in another list named Columns.
The data missing in employment_industry and occupation were due to them being unemployed so filled the null space with unemployed.
Also filled the missing data in health insurance as 0.
The features which had only two different values like male female etc i changed them to 0 and 1 manually.
I dropped the resondent_id because it wont affect the dataset as i also checked it it corresponds to the labels.
The dataset was highly unbalanced so i prefered to use robust model as xgboost classifier which doesnt depend on imbalance.
I also used pipeline from sklearn library and used OneHotEncoder to change the categorical columns.
I split the training set into train and test at 0.8 ratio two times for two different vaccines.
Inside the pipeline I passed preprocessor which changes the categorical columns as well fill the missing data.
I filled the missing numerical columns with mean and categorical columns with Most frequent data.
Now I checked that i have 105 columns so i checked the feature importance using random forest.After i got the important features list, I took features which are related highly and contribute direct 75% to target (after checking performance with several other parameters like top 15, 20 etc)
I also tuned the hyperparamters using randomisedSearchCv.
After fitting i made a classification report as well as roc auc curve.
Finally I used the same transformation with test data and submit the notebook.
