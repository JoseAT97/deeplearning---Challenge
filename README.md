# deeplearning---Challenge

# Alphabet Soup Deep Learning Report

## Overview of Analysis
The goal of this analysis was to use a neural network to predict whether applicants funded by the nonprofit Alphabet Soup are likely to be successful. A dataset of over 34,000 applicants was used to train a binary classifier and improve predictive accuracy to 75% or higher through various optimization techniques.
-- 

## Results

###  What variable(s) are the target(s) for your model?
- The target variable is `IS_SUCCESSFUL`, which indicates whether an applicant successfully used the funding they received.

###  What variable(s) are the features for your model?
- All columns except `EIN`, `NAME`, and `IS_SUCCESSFUL` were used as features after encoding.

###  What variable(s) were removed from the input data?
- The columns `EIN` and `NAME` were removed because they are identifiers and do not contribute to predictive performance.

---

## Compiling, Training, and Evaluating the Model

- **Model Architecture:**  
  The optimized model includes three hidden layers with 128, 64, and 32 neurons, respectively. ReLU was used as the activation function in all hidden layers to introduce non-linearity, and sigmoid was used in the output layer for binary classification.

- **Optimization Steps Taken:**
  - Increased the number of neurons and added a third hidden layer
  - Introduced Dropout layers with a 0.3 rate to reduce overfitting
  - Extended training to 150 epochs
  - Grouped rare categories in `APPLICATION_TYPE` and `CLASSIFICATION` using a higher threshold (1,000 instead of 500)

---

## Summary
The optimized neural network achieved an accuracy of about 74%, showing improvement over the initial model. These models often perform better on tabular data and offer easier interpretation and tuning.

