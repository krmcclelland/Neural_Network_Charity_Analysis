# Neural Network Charity Analysis
Neural Networks and Deep Learning Models

## Environment
* Tensorflow v. 2.4.1

## Overview 
1.  Compare the differences between:
    * Traditional Machine Learning Classification
    * Regression Models
    * Neural Network Models.
2.  Describe the Perceptron Model and its components.
3.  Implement Neural Network Models using TensorFlow.
4.  Explain how different Neural Network Structures change algorithm performance.
5.  Preprocess and construct datasets for Neural Network Models.
6.  Compare the differences between:
    * Neural Network Models
    * Deep Neural Networks.
7.  Implement Deep Neural Network Models using TensorFlow.
8.  Save trained TensorFlow models for later use.

## Purpose
A foundation, Alphabet Soup, wants to predict where to make investments.  The goal is to use Machine Learning and Neural Networks to apply features on a provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.  The initial file has 34,000 organizations and several columns that capture metadata about each organization from past successful fundings

## Results:

### Data Preprocessing
1.  What variable(s) are considered the target(s) for your model?   
    * Checking to see if the target is marked as successful in the DataFrame, indicating that it has been successfully funded by Alphabet Soup.  

2.  What variable(s) are the features of your model?    
    * The "Is Successful" column is the feature chosen for this dataset.

3.  What variable(s) are neither targets nor features, and should be removed from the input data?     
    * The EIN and NAME columns will not increase the accuracy of the model and can be removed to improve code efficiency. 

### Compiling, Training, and Evaluating the Model
1.  How many neurons, layers, and activation functions did you select for your neural network model, and why?    
2.  In the optimized model: 
    * Layer 1, started with 120 neurons with a relu activation
    * Layer 2, reduced to 80 neurons and continued with the relu activation 
    * Layer 3, Sigmoid activation is a better fit with 40 neurons 
    * Layer 4 with 20 neurons.    

![Pic 1]()
![Pic 2]()
![Pic 3]()
![Pic 4]()
![Pic 5]()
![Pic 6]()
![Pic 7]()
![Pic 8]()

3.  Were you able to achieve the target model performance?      
    * The target for the model was 75%, but the best the model could produce was 72.7%.

4.  What steps did you take to try and increase model performance?   
    * Columns were reviewed 
    * “Status” and “Special Considerations” columns were dropped as well as increasing the number of neurons and layers.  
    * Other activations were tried such as tanh, but the range that the model produced went from 40% to 68% accuracy.  
    * The linear activation produced the worst accuracy, around 28%.  The relu activation at the early layers and sigmoid activation at the latter layers gave the best results.
  
![Pic 9](Dev_1_and_2.PNG)   
![Pic 10](Dev3.PNG)    

### Summary:   
The relu and sigmoid activations yielded a 72.7% accuracy, which is the best the model could produce using the various number of neurons and layers.  The next step should be to try the random forest classifier as it is less influenced by outliers.   
