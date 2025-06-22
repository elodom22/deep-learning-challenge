# deep-learning-challenge
This challenge focuses on predicting the success of funding applicants using machine learning and neural networks. The goal is to develop a binary classifier that determines whether organizations funded by Alphabet Soup will likely succeed based on various attributes. The purpose is to enable better decision-making for funding allocation, helping Alphabet Soup invest in organizations with the highest likelihood of success.

### Key Steps:
1.	Data Preprocessing – Clean and transform the dataset using techniques like encoding categorical variables and scaling features.
2.	Neural Network Model – Build and train a deep learning model using TensorFlow and Keras to classify successful applicants.
3.	Model Optimization – Adjust features, layers, and hyperparameters to improve accuracy beyond 75%.
4.	Performance Evaluation – Analyze model accuracy, loss, and predictions to assess effectiveness.
5.	Report & Recommendations – Summarize insights, justify results, and suggest possible improvements.

### Data Preprocessing
#### Target Variable: 
* IS_SUCCESSFUL (1 = successful, 0 = unsuccessful).

#### Feature variable(s):
* NAME
* APPLICATION_TYPE
* AFFILIATION
* CLASSIFICATION
* USE_CASE
* ORGANIZATION
* STATUS
* INCOME_AMT
* SPECIAL_CONSIDERATIONS
* ASK_AMT

#### Variable(s) removed from the input data: 
* EIN and Name 

#### Feature variable: 
* NAME was brought back into the optomized model.

#### Compiling, Training, and Evaluating the Model
*	Total Hidden Layers (3):
     *   Layer 1: 100 neurons, relu activation
     *   Layer 2: 30 neurons, tanh activation
     *   Layer 3: 10 neurons, sigmoid activation
*	Output Layer: 1 neuron, Sigmoid activation

### Performance
#### Test Accuracy: 
* Accuracy improved from 72.5% to 79.6% after model optimization

#### Optimization Improvements: 
Initially both EIN and Name were dropped from the model. However, it was determined that excluding Names with only one appearance improved model performance considerably. Adding neurons (100, 30, 10) to the hidden layers, changing and adding an additional hidden layer type (relu > tanh > sigmoid) exhibited marked improvement from the original model.


### Conclusion
By optimizing the model, we achieved an accuracy exceeding 79%, meaning that 79% of the test data points were correctly classified. This indicates that an applicant has nearly an 80% probability of success if the following criteria are met:\
*	The applicant's name appears more than once (indicating they have applied more than once).
*	The application type belongs to one of these categories: T3, T4, T5, T6, or T19.
*	The application's classification falls under one of the following values: C1000, C1200, C2000, C2100, or C3000.

#### Alternative Approach: 
While this model demonstrated high accuracy and effectiveness, another viable option would be the Random Forest model, which is also well-suited for classification tasks.


