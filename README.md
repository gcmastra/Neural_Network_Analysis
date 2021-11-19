# Neural_Network_Analysis
Module 19 challenge

## Student: Christopher Mastrangelo

Optimizing Neural Networks is a process of trial and error.
What are the factors that contribute to determining the optimal accuracy rate with minimal loss? 
- Number of features (columns)
- Number of layers in the neural network
- Number of nodes in each layer
- Choice of the activation function in each layer

Determining which of these is more important takes multiple test runs isolating each variable one at a time.

Another factor that can affect the outcome is the exact split of the training data vs the testing data.
Selecting a different randomizer for the train_test_split function has an effect on the results even though it is small. 

In order of importance, the factor that affects the accuracy rate the most is the number of nodes in the layers.
Adding more layers does not necessarily increase performance, at least according to the course material.

These are the questions we attempted to answer: 

### Data Preprocessing
 - What variable(s) are considered the target(s) for your model? 
   <br><b>Answer: </b>Column "IS_SUCCESSFUL" is the target variable- it is binary yes/no that tells outcome on whether the funding was used successfully or not.
 - What variable(s) are considered to be the features for your model?  
 <br><b>Answer: </b>The following columns (variables) 

'APPLICATION_TYPE',
 'AFFILIATION',
 'CLASSIFICATION',
 'USE_CASE',
 'ORGANIZATION',
 'INCOME_AMT'

 - What variable(s) are neither targets nor features, and should be removed from the input data?
<BR>Answer: The columns EIN and NAME were dropped, as well as "SPECIAL_CONSIDERATIONS" to reduce the noise in the model.
 "SPECIAL_CONSIDERATIONS" semed like a good candidate to remove because it was only a binary 1/0 indicating whether there were special considerations in the application but not indicating what the considerations were.

 ### Compiling, Training, and Evaluating the Model
- How many neurons, layers, and activation functions did you select for your neural network model, and why?
 <br><br><b>Answer:</b> In the initial run, I used the same number of layers(3) and nodes(8,5,1) as in the example in the class materials section 19.4.4
 <br>In another run, I reduced the number of columns( features) while keeping the number of nodes the same
 <br>In another run, I increased the number of nodes in each layer by a factor of 10
 <br>
 <ul><li>Were you able to achieve the target model performance?</li>
 <br> <b>Answer: </b>I was able to improve the accuracy of the model from 0.5068 to 0.6281 but I was unable to achieve an accuracy rate > 0.75. The higher accuracy was achieved by increasing the number of nodes in layer 1.
 <br><br></ul>
<ul><li>What steps did you take to try and increase model performance?</li>
 <br><b>Answer: </b>As described above, changed the number of nodes in each layer, and dropped some columns to reduce the noise in the model to see the effect on model accuracy. The change that had the most impact was increasing the number of nodes in the layers. Reducing colmns/features improved accuracy but by much less. Changing the activation function was the third choice.</ul>
<br>
 
  ### Suggestions for Additional Optimizations
 
 The neural network might perform better if more of the non-numeric columns were dropped.  In addition to "NAME" and "EIN" which are arbitrary and should have no effect on performance, other subjective data like "Affiliation" or "Organization" could probably be removed from the model reducing the "noise" in the network.
 
 Two other intangible factors might be worth researching.  In the interest of time I was only able to include four(4) runs of the model with different numbers of nodes in the layers. If I had more time I would have also looked into these questions: 
 <ul>1. Change the number of bins- I would change the cut off point to fine tune how many classifications were grouped into the "Other" category.</ul>
 <ul>2. Changing the randomizer on the train_test_split() function.  Intuitively it shouldn't make a difference, but it does, because the randomizer is pseudo-random</ul>
 <ul>2. Changing the ratio of training to test data - instead of 75/25 which is the standard, I would try 80/20 to see how it affects the accuracy.</ul>
  
 <hr>

### Thank you for reading
