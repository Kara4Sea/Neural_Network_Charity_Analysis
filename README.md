# Neural Network Charity Analysis

## Overview of the analysis
The purpose of this analysis is to create a binary classifier to predict if an applicant will be successful after receiving funding from Alphabet Soup.

## Results

* Data Preprocessing
  * What variable(s) are considered the target(s) for your model? The target for the model is the "IS_SUCCESSFUL" column, as we are looking to predict if a prospective applicant will be successful or not.
  * What variable(s) are considered to be the features for your model? The variable considered to be the feature for our model is the "APPLICATION_TYPE" column.
  * What variable(s) are neither targets nor features, and should be removed from the input data? All other columns outside of "IS_SUCCESSFUL" and "APPLICATION_TYPE" are not relevent and can be removed.

  ![target_features](https://user-images.githubusercontent.com/110419577/216454219-a2ea3363-5e96-4b5d-9032-b4333d44d41d.png)


* Compiling, Training, and Evaluating the Model
  * How many neurons, layers, and activation functions did you select for your neural network model, and why?
   * Neurons - For the hidden layers, I selected 80 neurons for the first and 30 neurons for the second. For the classification output, I selected one neuron to produce a yes or no binary decision.
   * Layers - I selected two hidden layers. For the classification output, only one layer is needed.
   * Activation Functions - For the hidden layers, I selected ReLU to enable a nonlinear relationship. For the classification output, I selected sigmoid to provide a probability output.

  ![neurons_layers_activation functions](https://user-images.githubusercontent.com/110419577/216454353-5ff9b78f-82dc-40b5-9eb4-78ead396ea1e.png)

  * Were you able to achieve the target model performance? No, I was not able to acheive the target model performance of 0.75. Original accuracy results came in at 0.45. And thought the optimized results were improved, they came in under the target model performance at 0.58.
  
  ![accuracy_orig](https://user-images.githubusercontent.com/110419577/216454386-44fa6c7b-6800-43c9-85e5-fad2659f1145.png)
  ![accuracy_optimized](https://user-images.githubusercontent.com/110419577/216454401-ff039949-8993-4b65-ba3c-da161652fd90.png)

  
  * What steps did you take to try and increase model performance? In an attempt to increase model performance, I took several steps. First, I dropped additional columns including "STATUS" and "ASK_AMT". Next, I created more bins for rare occurrances in columns, by expanding from <500 to <20. Additionally, I created a third hidden layer and increased the number of neurons on the two original hidden layers.

  ![optimize_drop_columns](https://user-images.githubusercontent.com/110419577/216454482-189863d2-bb6a-4780-a197-df8152e6da28.png)
  ![optimize_bins](https://user-images.githubusercontent.com/110419577/216454502-43e586d4-1d84-42c4-b886-f9045e549221.png)
  ![optimize_define_model](https://user-images.githubusercontent.com/110419577/216454530-4684fdb4-3dac-4542-b502-b6525787484e.png)

## Summary
The overall results of this analysis confirm that this deep learning model was not successful in accurately predicting the sucess rates in applicants. Soem tweaks to the model may serve to improve the model performance to meet or exceed the target model performance. I would recommend a combination of adding more hidden layers and using different activation functions for the hidden layers to see if an improved model performance score could be found.
