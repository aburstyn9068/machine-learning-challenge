# machine-learning-challenge
Machine Learning Project

This respository contains the code files for a manchine learnining model that uses data collected from the NASA Kepler telescope to classify the probability of the data being a discovered hidden planet outside of our solar system.

The code is written in Python and uses the Scikit-Learn, Tensorflow, and Keras libraries.

The models were created using a similar pipleine structure. First the number of independent variables was reduced to the 20 most important features. The 20 best features were selected using Scikit-Learn's feature selector. The variables were ranked using the F-value. F-value was selected because it allowed for negative numbers to be included (where as chi2 can only be used for non-negative numbers).

The categorical data (dependent variable) was converted into a numerical vector using one-hot-enconding.

Next, the data was split into a training and testing set to allow the model to be evaluated by predicting the results of the unseen data from the testing set.

The data was then preprocessed by normalizing it using a Min/Max Scaler.

The model was then created and fit using the training data to get a baseline score. A cross validation grid search was then performed to find the optimal parameters and hypertune the model.

The model that produced the highest accuracy on the testing set was then saved.

The three models that were created were:
    1. K-Nearest Neighbors (86% accuracy)
    2. Neural Network/Deep Neural Network (90% accuracy)
    3. Random Forest Classifer (89% accuracy)

The best model was the Deep Neural Network with 90% accuracy. The random forest classifier was almost equally as accurate at just under 90%. With a model that accurate, it would be worthwhile to investigate a potential new planet if the model deems the conditions appropriate.

One way to improve the accuracy of the model can be a deeper investigation into the input variables and possible multicolinearity that may exist between the variables. An effective way (although expensive in computing power/time) to find the optimal combination of input variables is through an exhaustive recursive feature search. The exhaustive feature selection process can test the accuracy of the model on all the possible combinations of input varaibles and select the combination that results in the highest accuracy.

