# Neural Network Charity Analysis

## Overview

Alphabet Soup has provided a data set containing 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization:

- `EIN` and `NAME` — Identification columns
- `APPLICATION_TYPE `— Alphabet Soup application type
- `AFFILIATION`— Affiliated sector of industry
- `CLASSIFICATION`— Government organization classification
- `USE_CASE` — Use case for funding
- `ORGANIZATION` — Organization type
- `STATUS` — Active status
- `INCOME_AMT` — Income classification
- `SPECIAL_CONSIDERATIONS` — Special consideration for application
- `ASK_AMT` — Funding amount requested
- `IS_SUCCESSFUL` — Was the money used effectively

## Purpose

The purpose of this analysis is to use the features and create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

# Results

### Data Preprocessing

The following variable is considered the target for the model:
- `IS_SUCCESSFUL`

The following variables are considered features for the model:
- `APPLICATION_TYPE`
- `AFFILIATION`
- `CLASSIFICATION`
- `USE_CASE`
- `ORGANIZATION`
- `STATUS`
- `INCOME_AMT`
- `SPECIAL_CONSIDERATIONS`
- `ASK_AMT`
- `IS_SUCCESSFUL`

The following variables have been disregarded from the dataset since they are neither targets nor features:
- `EIN`
- `NAME`

### Compiling, Training, and Evaluating the Model

Number of neurons, layers, and activation functions selected for the neural network model:
- The original model has two hidden layers. The first layer has 80 neurons, and the second layer has 30 neurons in which both layers use `relu` activation functions. This model produced an accuracy of 72.56%

The following adjustments were made to optimize and increase model performance:
- Two features were removed
    - `USE_CASE`
    - `STATUS`
- A third hidden layer containing 5 neurons was added
- An additional 5 neurons were added for the first and second hidden layer

# Summary

Even after adjusting the model to optimize and increase accuracy, my model was not able to achieve a predictive accuracy rate of 75%. Adding more layers and neurons only improved accuracy rate by 0.14%, bringing it up to 72.70%. Thus, it's better to keep a simpler model than overcomplicating the neural network with more hidden layers and neurons. The complexity of the neural network should match the complexity of the dataset provided.

To solve this classification problem, I recommend using a different binary classifier, specifically the support vector machine (SVM) over a logistic regression. The risk of overfitting is less in SVM, while Logistic regression is vulnerable to overfitting.



