# Team name & members
Team name: house pricing

Yue Lin ; Ziqing Chai

# project: Kaggle-House-Prices-Advanced-Regression-Techniques
Ask a home buyer to describe their dream house, and they probably won't begin with the height of the basement ceiling or the proximity to an east-west railroad. But this playground competition's dataset proves that much more influences price negotiations than the number of bedrooms or a white-picket fence.

With 79 explanatory variables describing (almost) every aspect of residential homes in Ames, Iowa, this project give you predict to the final price of each home.

# Acknowledgments
The Ames Housing dataset was compiled by Dean De Cock for use in data science education. It's an incredible alternative for data scientists looking for a modernized and expanded version of the often cited Boston Housing dataset. 

# Milestone 1
We have done linear regression, decision tree and randome forest for the prediction of hourse pricing.
First we drop features which contains too many NaN values, and then do data processing for the rest of features. In the data processing, we dummy the categorical features into 1 or 0, impute missing value of numerical features with median and z-score them. 

Secondly, we implement the 10-fold-cross-validation on linear regression, decision tree and random forest with the error measure of RMSE. The results are 34539.1615156, 38321.2152159, 31976.8441112 respectly.

# Milestone 2
We have done gaussain process with 2 different kernels of rbf and dot product and SVM to do the hourse pricing prediction. We use the same data processing methods as milesone 1 and do the 10-fold-cross-validation to evaluate the results. For error measure, we also use RMSE. 

For gaussain process, we also draw the coeffients of variants in each fold of test to show the uncertainty of each prediction. The whole picture contains the true values-red points, predictions-blue poitns and uncertainties-blue area. Therefore, we can get 10 pictures for each keneral and it's easy for us to see the performance of using those gaussian process. The results of using rbf kernel is 38828.0679446 and using dot product kenerl is 34292.8709243 with smaller uncertainty overall showed by picture.

We use soft margin svm and the result is 81407.3263723.
