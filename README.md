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

# Milestone 3
We have done PCA and SVD for dimensionality reduction for our training data. Since the biger score of eigenvalue the more important that dimension can be, we plot the firgue of first 100 eigenvalues(descending order) and calculate the number of eigencalues that contains 90% information for both methods. In PCA, we choose the first 28 eigenvalues and in SVD, we choose the first 107 eigenvalues. Then transform the original data to the projection to the new dimensionality calculated by PCA and SVD to form our new training data. 

We also have accomplished neural network with our full dataset and the dataset after using PCA and SVD dimensionality reduction. Performance comparisons(RMSE) are as following.

|  | full-data | PCA | SVD |
| -------------| ------------- | ------------- | ------------- |
| Linear Regression | 34539.1615156  | 34484.0908176  | 32017.0904093  |
| Random Forest | 31976.8441112  | 31216.2050758  | 32260.5613001  |
| Gaussian Process (dot product) | 34292.8709243  | 34499.0931218  | 31971.9657388 |
| Neural Network | 31103.6747775  | 34864.4405225  | 31542.5468814 |

# Milestone 4
|  | Linear Regression | Random Forest | GaussianProcess | SVM | Neural Network |
| -------------| ------------- | ------------- | ------------- | ------------- | ------------- |
| Split1(seed=0) | 36413.526238045808  | 31567.423190530259  | 38294.871308481321 | 81436.989616305844 |  |
| Split2(seed=1) | 36341.756394955912  | 31244.790496499365  | 38090.700223078369 | 81399.875248219076 |  |
| Split3(seed=2) | 36074.309327954026  | 32762.678224426258  | 38417.281029440644 | 81479.267129689382 |  |
| Split4(seed=3) | 33227.582853984146  | 30757.804162477674  | 38882.640119526004 | 81353.588770489048 |  |
| Split5(seed=4) | 35870.249357741181  | 31445.005291189322  | 38184.771761052958 | 81405.828667334936 |  |
| Split6(seed=5) | 34719.421381387263  | 30800.142268024811  | 38435.372360825619 | 81442.490036629766 |  |
| Split7(seed=6) | 35159.551168313563  | 30843.783234457231  | 38282.187020039717 | 81361.988452384001 |  |
| Split8(seed=7) | 35088.459111640688 | 29489.873783983909  | 37939.020293418631 | 81457.12574393602 |  |
| Split9(seed=8) | 34579.786308538489  | 29864.977965871894  | 38602.408654445921 | 81505.431786348243 |  |
| Split10(seed=9) | 34257.318015019016  | 28865.995598385663  | 38705.307291369601 | 81454.912327761398 |  |
