# Neural_Network_Charity_Analysis
Neural Network project for UT Austin Data Analysis Certificate

## Overview
We were presented with a dataset of non-profit donation outcomes and were asked to create a neural network model that could predict which organizations would achieve satisfactory outcomes with the money given to them.

## Results
- Data Preprocessing
For our maodel's targets, we used the "IS_SUCCESSFUL" variable. We used the other variables (APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT) for the model's features. We removed "NAME" and "EIN" from the model because they are identifiers and are not relevant to the outcome.

- Compiling, Training, and Evaluation
To begin with, we used two hidden layers with 8 and 5 neurons, respectively. In later iterations we increased this to three hidden layers with 15, 10, and 5 neurons each in an attempt at greater accuracy. We tried various different activation functions, but ReLU seemed to be the most effective. We used a Sigmoid activation function for the output layer because we are performing a binary classification. We were never quite able to achieve the target performance of 75%. The closest we could get was 72%. In order to enhance the model we experimented with various hidden layer, neuron counts, and activation functions. We also adjusted our preprocessing methods. In some cases we left out features. In other cases we incorporated each and every feature available into the model. We also adjusted the binning of the features, reducing the number of low-count bins in order to simplify the model and increase accuracy.

## Summary
Overall this model performed well, although it never quite achieved the 75% accuracy we desired. A different model, such as a Random Forest Classifier model, might be able to solve this problem with close to the same accuracy and require less computing. This seems like a good problem for a Random Forest model because the data is in integer form and the solution we are looking for is a binary classification. A Random Forest model would be able to apply weak models to each of the features and come to a stronger prediction by combining each of those weak models.