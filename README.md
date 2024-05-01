# Feature_Selection
This repository contains Python implementation of various feature selection techniques. Feature selection is a critical step in machine learning, aimed at identifying the most relevant features for modeling and prediction tasks. The implemented methods encompass a range of strategies, each with its own strengths and applications.

## Why Feature Selection?
- Data Understanding
- Reduced storage requirement as data size is reduced
- reduced computational process time
- makes learning easier
  
Search space 2^w w= number of features

## Implemented Feature Selection Methods:
wrapper, filter, embedded, and hybrid methods
1. Wrapper
    1. The predetermined learning algorithm  decides the quality of selected features based on the evaluation metric defined
    2. More accurate than filter methods 
    3. Dependent on the learning algorithm
    4. Examples: 
        1. forward feature selection
        2. Backward feature Elimination
        3. Exhaustive feature selection: a brute-force evaluation of each feature subset (most robust)
        4. Recursive Feature Elimination (external estimator that assigns weights to feature) 
            1. the least important features are pruned from the current set of features and a recursively smaller and smaller set is obtained till the desired number of features remain in the set
2. Filter
    1. Apply Statistical measures to evaluate the set of attributes focusing on the intrinsic properties of the features
    2. Faster than wrapper methods
    3. This can be termed as General purpose F S
    4. Examples :
        1. Information Gain
        2. Chi-Square Test
        3. Fisher Score
        4. Correlation Coefficient
        5. Variance Threshold (removes feature whose variance doesn’t meet threshold based on entropy principle: higher the variance higher the information)
        6. MAD: mean absolute difference from mean value of the feature
        7. Dispersion ratio: Arithmetic Mean / geometric mean — > higher the dispersion more the relevance 
        8. mRMR : minimum redundancy maximum relevancy I(x,y) - I(xi,xj)*1/num features
        9. 
3. embedded
    1. Model fitting and Feature selection simultaneously
       These methods incorporate feature selection as part of the model training process itself.
    3. Examples :
        1. Lasso regression L1  regularize: in a way that least important features coeff = 0 
        2. RandomForest Importance (random forests naturally rank by how well the feature improves the purity of the node or decreases impurity i.e. Gini index)


# Contributions:
Contributions to this repository are welcome! If you have ideas for additional feature selection methods or improvements to existing ones, feel free to submit a pull request.
