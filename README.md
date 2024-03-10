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
- **Steps Taken to Optimize the Model:**
    1.  Checked the ASK_AMT column for outliers. There were 8,000 outliers out of approximately 34,000 rows of data. Removed any rows with ask amounts over the upper bound of the data set.
        - In the future, I would try to break this column down into bins to keep all rows in the data
    2.   For the APPLICATION_TYPE and CLASSIFICATION columns, used the `value_counts` function to determine how many of each value were in the column and bucketed the smaller groups together into an "Other" value
    3.   Added an additional hidden layer to the neural network to increase the consideration of interactions between variables
