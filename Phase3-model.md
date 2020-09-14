# Phase 3: Data Preparation Tasks and Modeling

## Final Dataset Selection
1. Analyze constraints:
e.g. beware of the final dataset properties. Total size, columns, record selection, data type

## Preparing the data
1. Cleaning
e.g. Missing data?
2. Transforming
3. Merging
4. Formatting
5. Labeling


## Modeling
1. Model selection and creation
- Decide which ML method is going to be used?
    - supervised learning
    - unsupervised learning
    - deep learning
    - reinforcement learning
e.g. DNN? random forest? Modeling techniques, constraints

2. which framework to work on?
- mature level framework:
    - tensorflow
    - pytorch
    - mxnet
- intro level framework:
    - aws sagemaker
    - azure machine learning
    - databricks sparkML


3. Model training plan
e.g. use what to evaluation the model? (objective matrix)

4. Hyper-parameter tuning/testing?
- Manual: Defaults, guess and check. requires experience, intuition and heuristics
- Brute Force: Grid search, random search, sobol
- Meta model: Build another ML model to predict hyperparameters of the first ML model
    - Gaussian process regression models + Bayesian optimization
    - e.g. sigopt, gpyopt, for hyprt-parameter tuning?
