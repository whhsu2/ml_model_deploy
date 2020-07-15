## Machine Learning Model Pipeline Overview

1. Gather Data Sources
2. Data Analysis
3. Feature Engineering
4. Feature Selection
5. Machine Learning Model Building
5. Model Building Buisness Uplift Evaluation
6. Model Deployment 

### Feature Engineering 

    1. Missing data: Missing values within a variable
    2. Labels: Strings in categorical variables
        * Cardinality: high number of labels
        * Rare Labels: infrequent categories
    3. Distribution of Variables: Normal vs skewed 
        * Linear model assumptions: Normal distribution
    4. Outlier: Unusual or unexpected values

### Feature Selection
Why do we select features:  

    1. Simple models are easier to interpret  
    2. Shorter training time  
    3. Enhanced generalization by reducing overfitting  
    4. Easier to implement by software developers -> model production  
    5. Reduced risk of data errors during model use
    6. Data Redundancy    

How do we select features:  

    1. Embedded methods  
    2. Wrapper methods  
    3. Filter methods  

### Model Building 
How to evaluate model performance: 

    1. ROC-AUC    
    2. Accuracy  
    3. MSE,   


## ML Architectures

### Key Principles for ML System Architecture
    1. Reproducibility: Have the ability to replicate a given ML prediction
    2. Automation: Retrain, update and deploy models as part of an automated pipeline
    3. Extensibility: Have the ability to easily add and update models
    4. Modularity: Preprocess/feature engineering code used in training should be organized into clear pipelines
    5. Scalability: Ability to serve model predictions to large numbers of customers
    6. Testing: Test variations between model versions


### General ML Architectures
    1. Train by batch, predict on the fly, serve via REST API
    2. Train by batch, predict by batch, serve through a shared database
    3. Train, predict by streaming
    4. Train by batch, predict on mobile 

### Architecture Component Breakdown
    **Data layer**: The data layer provides accesss to all of our sources which simplifies the challenge of data reproducibility
    **Feature layer**: The feature layer is responsible for generating feature data in a transparent, reusable, and scalable manner
    **Scoring layer**: The scoring layer transforms features into predictions. 
    **Evaluation layer**: The evaluation layer checks the equivalence of two models. This layer can be used to monitor production models, e.g. to check how closely the predictions on live traffic matches the training predictions.
    