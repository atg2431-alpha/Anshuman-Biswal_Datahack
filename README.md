I opened the training features set and checked the columns and data .
I found some categorical columns i separated it in another list named Columns.
The data missing in employment_industry and occupation were due to them being unemployed so filled the null space with unemployed.
The features which had only two different values like male female etc i changed them to 0 and 1 manually.
I dropped the resondent_id because it wont affect the dataset as i also checked it it corresponds to the labels.
The dataset was highly unbalanced so i prefered to use robust model as xgboost classifier which doesnt depend on imbalance.
I also used pipeline from sklearn library and used OneHotEncoder to change the categorical columns.
I split the training set into train and test at 0.8 ratio two times for two different vaccines.
Inside the pipeline I passed preprocessor which changes the categorical columns as well fill the missing data.
I filled the missing numerical columns with mean and categorical columns with Most frequent data.
I also tuned the hyperparamters using randomisedSearchCv.
After fitting i made a classification report as well as roc auc curve.
Finally I used the same with test data and submit the notebook.
