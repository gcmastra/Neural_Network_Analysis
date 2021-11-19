# Neural_Network_Analysis
Module 19 challenge

## Student: Christopher Mastrangelo

Optimizing Neural Networks is a process of trial and error.
What are the factors that contribute to determining the optimal accuracy rate with minimal loss? 
- Number of features (columns)
- Number of layers in the neural network
- Number of nodes in each layer

Determining which of these is more important takes multiple test runs isolating each variable one at a time.

Another factor that can effect the outcome is the exact split of the training data vs the testing data.
Selecting a different randomizer for the train_test_split function has an effect on the results even though it is small. 

In order of importance, the factor that affects the accuracy rate the most is the number of nodes in the layers.
Adding more layers does not necessarily increase performance, at least in my test runs.

These are the questions we attempted to answer: 

### Data Preprocessing
 - What variable(s) are considered the target(s) for your model? <br>Answer: column "IS_SUCCESSFUL" is the target variable
 - What variable(s) are considered to be the features for your model?  <br>Answer: the following columns (variables) 

'APPLICATION_TYPE',
 'AFFILIATION',
 'CLASSIFICATION',
 'USE_CASE',
 'ORGANIZATION',
 'INCOME_AMT'
 <br>some stuff got deleted, try again later. there is no undo button while editing
 
 - What steps did you take to try and increase model performance?  
    <br>Answer: tbd

Thank you for reading
