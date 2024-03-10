# Alphabet Soup Deep Learning Model Analysis
## Overview
The purpose of this analysis is to develop a neural network model with a 75% accuracy minimum that can predict which Alphabet Soup applicants will be successful with their funds based on a variety of features.
## Results
### Data Preprocessing
- **Target Variable:** IS_SUCCESSFUL
- **Feature Variables:**
  - APPLICATION_TYPE
  - AFFILIATION
  - CLASSIFICATION
  - USE_CASE
  - ORGANIZATION
  - STATUS
  - INCOME_AMT
  - SPECIAL_CONSIDERATIONS
  - ASK_AMT
- **Removed Variables:**
  - EIN
  - NAME
### Compiling, Training, and Evaluating the Model
![image](https://github.com/lvit001/deep-learning-challenge/assets/140283164/4b8286f2-4f07-4a8b-aee5-b34245e26add)
- **Total Number of Layers:**
  - 3 Hidden Layers
  - 1 Output Layer
- **Breakdown of each Layer:**
  -   **1st Hidden Layer:** 50 Neurons, Relu Activation Function
      - _This layer has the highest number of neurons as it is the first layer. It utilizes the relu function since it is the fastest at learning and provides simplified outputs_
  -   **2nd Hidden Layer:** 25 Neurons, Relu Activation Function
      - _This layer has the second-highest number of neurons as it is the second layer, and I am decreasing the amount of neurons with each hidden layer. I choose to use the relu function for the same reasoning as above.
  -   **3rd Hidden Layer:** 10 Neurons, Relu Activation Function
      - _This layer has the second-lowest number of neurons as it is the third and final hidden layer. **It utilizes the relu function since it is the fastest at learning and provides simplified outputs_ **
  -   **Final Output Layer:** 1 Neuron, Sigmoid Activation Function
      - _This is the final layer, the output layer, which only has one neuron as the neuron as this neuron represents the final prediction. The sigmoid activation was utilized as the target variable is binary between 0 and 1. The sigmoid function transforms outputs into a value between 0 and 1._
- **Was the target model performance achieved?**
  - **Yes**, the model had an accuracy higher than 75% once it was optimized.
