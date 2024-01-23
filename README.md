# deep-learning-challenge
This is my UT Bootcamp Module 21 Challenge

# Neural Network Model Report
## Overview of the analysis
This analysis is intend to create a tool that can help a nonprofit foundation 'Alphabet Soup' to select the applicants for funding with the best chance of success in their ventures. Based on a CSV from Alphabet Soup’s business team, which contains more than 34,000 organizations that have received funding from Alphabet Soup over the years, this analysis creates a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

## Results: 
Using bulleted lists and images to support your answers, address the following questions:

### Data Preprocessing
* `IS_SUCCESSFUL` column is the target for the model.
* `APPLICATION_TYPE`, `AFFILIATION`, `CLASSIFICATION`, `USE_CASE`, `ORGANIZATION`, `STATUS`, `INCOME_AMT`, `SPECIAL_CONSIDERATIONS` and `ASK_AMT` are the features for your model initially. During the optimization attempts, `STATUS` and `SPECIAL_CONSIDERATIONS`, are removed from features variables.
* `EIN` and `NAME` should be removed from the input data because they are neither targets nor features.

### Compiling, Training, and Evaluating the Model
* There are totally 3 layers built in the model:
    * First layer (Hidden layer) has 80 neurons, and `'relu'` is selected as its activation function.
    * Second layer (Hidden layer) has 30 neurons, and `'relu'` is selected as its activation function.
    * Third layer (Output layer) has 1 neurons, and `'sigmoid'` is selected as its activation function.
    * The numebr of hidden layers and neurons are actually randomly tries. After a few attempts adjustments, 2 hidden layers with 120 neurons can result in a better preformance. The actvation function selection is based on the analysis of the given data, which is positive, nonlinear data.For the output layer, the activation function is used to classify a binary result, so `'sigmoid'` is selected.

* After more than 3 attempts to optimize the model, the target model performance of 75% accuracy still not able to achieve.

* Steps that were taken in your attempts to increase model performance:
    * Step 1: Dropping more or fewer columns. (e.g. dropping `STATUS` and `SPECIAL_CONSIDERATIONS`)
    * Step 2: Creating more bins for rare occurrences in columns. (e.g. creating more bins for occurrences in  `APPLICATION_TYPE` and `CLASSIFICATION`)
    * Step 3: Add more hidden layers, as well as change numbers of neurons to a hidden layer.

## Summary:
The overall results of the deep learning model has a 73% accuracy and 56.43% loss, which means it could predict correctly in 73% from the data, while it can make some big errors in those incorrect predictions. After trying 3 attempts to increase the model performance, I suggest to input more data so that the model can be trained with more data samples. We tried to eliminate the columns to lower the noise of the dataset, and also tried to give the model more bins for classifcation, and adjusted the model structure. However, none of these attempt has notable change on prediction accuracy. One better way to optimize the model is to use a larger sample dataset.  