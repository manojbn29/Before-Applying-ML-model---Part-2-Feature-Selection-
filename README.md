# Before-Applying-ML-model---Part-2-Feature-Selection-

We do the feature selection i.e we select the important features and apply that features to the ml model to get good accuracy score and to avoid curse od dimensionality.

Always we first do train test split and then we will apply the feature selection technique to avoid the overfitting.

Before going to the types to get more info please read the 'Feature Selection info' file in this repoistory

There are so many types of feature selection below are some:

1) Removing features with low variance (VarianceThreshold)
2) Univariate feature selection:

            a) For regression: f_regression, mutual_info_regression
            b) For classification: chi2, f_classif, mutual_info_classif
 
3) Correlation Matrix (Using Pearson correlation)
4) Recursive feature elimination
5) Feature selection using SelectFromModel:

            a) L1-based feature selection:
                    a.1) Regression : Lasso
                    a.2) Classification : LogisticRegression and Linear SVM
                    
            b) Tree-based feature selection
            
6) Sequential Feature Selection
7) Feature selection as part of a pipeline


## There are so many techniques to extract the features:

1) Filter method:

![image](https://user-images.githubusercontent.com/84167701/122674809-55677100-d1f4-11eb-8c79-e653162e7911.png)

2) Wrapper method:

![image](https://user-images.githubusercontent.com/84167701/122674891-a5dece80-d1f4-11eb-8647-46c63d501d22.png)

3) Embedded method:

![image](https://user-images.githubusercontent.com/84167701/122674903-bee77f80-d1f4-11eb-8b80-d1f9d049480e.png)



1) Forward Selection: Forward selection is an iterative method in which we start with having no feature in the model. In each iteration, we keep adding the feature which best improves our model till an addition of a new variable does not improve the performance of the model.

2) Backward Elimination: In backward elimination, we start with all the features and removes the least significant feature at each iteration which improves the performance of the model. We repeat this until no improvement is observed on removal of features.

3) Recursive Feature elimination: It is a greedy optimization algorithm which aims to find the best performing feature subset. It repeatedly creates models and keeps aside the best or the worst performing feature at each iteration. It constructs the next model with the left features until all the features are exhausted. It then ranks the features based on the order of their elimination.
