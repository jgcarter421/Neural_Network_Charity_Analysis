# Neural Network Charity Analysis
## Overview
The purpose of this analysis is to create a neural network model that is capable of predicting whether a company will be successful if funded by a charitable organization, Alphabet Soup.  For this analysis to work the following methods were used:
* Preprocessed the data.
* compiled, trained, and evaluated the model.
* Optimized the model.

## Results
### Preproccessing the Data
* The columns "EIN" and "NAME" are neither targets nor features, and were removed from the data.
* The column "IS_SUCCESSFUL" became the target of the data.
* The columns "APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION", "STATUS", "INCOME_AMT", "SPECIAL_CONSIDERATIONS", and "ASK_AMT" became the features of the model.  These features were then encoded, split into training and testing data, and the data was standardized to be run through the neural network model.

### Compiling, Training, and Evaluating the Model
* Initially, the nueral network model consisted of two hidden layers with 80 and 30 neurons respectively.  I attempted to use between two and three times the number of nodes as input features, as this typically works best for deep-learning models.  The activation function for the hidden layers was "relu."  The output layer has one input, and an activation function of "sigmoid."
  * After running, this model, the model's performance was only 73%, which isn't ideal for predicting the outcome for investing in a company.
  
* Next, in order to optimize the model, I added more nodes to the hidden layers (100 and 50 respectively).  This still gave an accuracy of 73%.
* I then added a third hidden layer with 20 nodes.  This, again, gave an accuracy of 73%.
* In the third attempt to optimize the model, I changed the activation function of the output layer to "tanh,' which still gave an accuracy of 73%.
* In the fourth attempt, I added a fourth hidden layer, which gave the same result, 73% accuracy.
* I also changed the activation function of the hidden layers to "tanh," and kept the activation function of the output layer as "sigmoid."  This resulted in the same accuracy of 73%.

## Summary
The model, even after attempting to optimize it, only achieved 73% accuracy.  It appears that as the data passes through the neurons of the hidden layers, the data is becoming overfitted.  In order to avoid overfitting the model, more features could have been removed, or more data added to the data set.  With the target goal of 75% accuracy, and the model coming up short with only 73% accuracy, an Ensemble Learing Random Forest classifier could have been used for better accuracy at predicting the outcome.  This is because Random Forests are robust against overfitting the data, can rank the importance of the input variables in a natural way, can handle thousands of input features without deletion, and can handle large data sets.  Random Forest classifiers also are much faster, and cheaper, than running deep learning neural network models.  
