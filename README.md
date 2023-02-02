# Neural Network Charity Analysis

## Overview of the analysis
The purpose of this analysis is to create a binary classifier to predict if an applicant will be successful after receiving funding from Alphabet Soup.

## Results

* Data Preprocessing
  * What variable(s) are considered the target(s) for your model? The target for the model is the "IS_SUCCESSFUL" column, as we are looking to predict if a prospective applicant will be successful or not.
  * What variable(s) are considered to be the features for your model? The variable considered to be the feature for our model is the "APPLICATION_TYPE" column.
  * What variable(s) are neither targets nor features, and should be removed from the input data? All other columns outside of "IS_SUCCESSFUL" and "APPLICATION_TYPE" are not relevent and can be removed.

* Compiling, Training, and Evaluating the Model
  * How many neurons, layers, and activation functions did you select for your neural network model, and why?
  * Were you able to achieve the target model performance? No, I was not able to acheive the target model performance of 0.75. Original accuracy results came in at 0.45. And thought the optimized results were improved, they came in under the target model performance at 0.58.
  * What steps did you take to try and increase model performance? In an attempt to increase model performance, I took several steps. First, I dropped additional columns including "STATUS" and "ASK_AMT". Next, I created more bins for rare occurrances in columns, by expanding from <500 to <200. Additionally, I created a third hidden layer and increased the number of neurons on the two original hidden layers.

## Summary
The overall results of this analysis confirm that this deep learning model was not successful in accurately predicting the sucess rates in applicants. Soem tweaks to the model may serve to improve the model performance to meet or exceed the target model performance. I would recommend a combination of adding more hidden layers and using different activation functions for the hidden layers to see if an improved model performance score could be found.
