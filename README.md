# Model Training Report

## Overview
### The Purpose: 
This neural network is designed to be used as a tool for a nonprofit organization for predicting applicants with high chances of success to allocate funding to in hopes of creating a better method of selection for the organization.

# Data Preprocessing
* This model is built to target the "IS_SUCCESSFUL" variable of the data frame
* The "EIN" and "NAME" Columns are dropped initially to remove any non features for the model that can't be used for training or as categorical data
* once "EIN" and "NAME" are dropped, every remaining variable in the data frame is usable as a feature for training and testing.

# Results 

## Compiling, Training, and Evaluating the model

### Attempt 1
![attempt 1](https://github.com/JamesDraper59/deep-learning-challenge/assets/60665765/93cd401e-749f-43d7-9c35-da1e27c243de)

* The first attemp at refining and optimizing this model consisted of changing both the amount of neurons to be proportional and using a different activation function. this raised the accuracy from .72 up to .73 using 100 epochs

### Attempt 2
![attempt 2](https://github.com/JamesDraper59/deep-learning-challenge/assets/60665765/4e4258b4-9e55-4278-90d7-3d95dca665a4)

* The second attempt uses a third added layer with a higher ceiling on neurons with a gradual change, after returning back to the relu activation function and using 100 epochs for this model, it reverted back towards .72 accuracy, letting me know i was moving in the wrong direction.

### Attempt 3
![attempt 3](https://github.com/JamesDraper59/deep-learning-challenge/assets/60665765/5ee0c0e7-2617-4396-918b-90e24483f6ed)


* for my third attempt at optimization, i restructured my layers, reverted back to the tanh function, and altered my bins to try and make the data cleaner for the model

![name_bin](https://github.com/JamesDraper59/deep-learning-challenge/assets/60665765/eeed38e9-b4a2-4271-9839-63b69cb14668)

* instead of dropping the name column in the data frame as the assignment initially asks, i allowed it to stay for consideration that some applicants had far higher prevelance in the data set than others, a point which the model may be able to work with

![smaller_bin](https://github.com/JamesDraper59/deep-learning-challenge/assets/60665765/683bf1d2-689f-402f-8532-2e7137807dd8)

* and finally, i altered the size of the bins in my data from the initial set, deciding to compress them to higher figures with less space and variance between them. this allowed my model to reach the desired target of .75 accuracy, therefore fulfilling the ask show in this figure.

![final_model_accuracy](https://github.com/JamesDraper59/deep-learning-challenge/assets/60665765/f39b86bb-14f6-409f-80a9-ad16ff8e184f)

# Summary

## Overall Results:
 The model overall performs to expectations and desired requirements. it reaches the demanded accuracy and maintains a simple design that isn't difficult to understand for any potential operators. as for any other model i'd reccomend for this task, Random Forest could potentially handle the data better as it typically is less influenced by statistical outliers and tends to not have issues with any heterogeneous features.


  
