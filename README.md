# Neural_Network_Charity_Analysis

**OVERVIEW**

This project was created for us to predict if Charities were to receive funding if they would be successful or not. Seems like a silly question when you think about it, as in why wouldn't they be successful? Doesn't more money automatically mean success? NO. No it does not. You will find in the analysis below we predict success or not for these charities.


Within this project we used a handful of tools.

- Jupyter Notebook
- Tensor Flow Keras Sequential
- Pandas
- Matplotlib

These tools helped us dig deeply into the csv file we had at hand. 

**ANALYSIS/RESULTS**

**DATA PROCESSING**

What variable(s) are considered the target(s) for your model?

- The main variable that is considered the target of our model was IS_SUCCESSFUL.

What variable(s) are considered to be the features for your model?

- The variables that are considered to be the features of our model were; 
1. APPLICATION_TYPE
2. AFFILIATION
3. CLASSIFICATION
4. USE_CASE
5. ORGANIZED
6. STATUS
7. INCOME_AMT
8. SPECIAL_CONSIDERATIONS
9. ASK_AMT

What variable(s) are neither targets nor features, and should be removed from the input data?

- We started off my removing the EIN and the NAME variables.
- We also ended up dropping the APPLICATION_TYPE and CLASSIFICATION that had a handful of unique values.

**COMPILING, TRAINING, AND EVALUATING**

In order to achieve the oal of 75% accuracy I needed to compile, train and evaluate the model more than once. I was not able to get to a 75% accuracy but I did run 4 different trial models which I will discuess in detail below.

# BASE MODEL

I dropped the EIN and NAME from the table, and consolidated the APPLICATION_TYPE variable.

- Hidden nodes layer 1 = 80
- Hidden nodes layer 2 = 30
- Output nodes = 1
- Hidden Layer Activation = RELU
- Output Layer Activation = SIGMOID
- EPOCHS = 100

- ACCURACY = .7320
- LOSS = .5537

This model did not achieve the target goal.


# OPTIMIZATION TRIALS

**TRIAL 1**

Increasing the epchos to 200 instead of 100 from the 1st and 2nd deliverable.

- Hidden nodes layer 1 = 80
- Hidden nodes layer 2 = 30
- Output nodes = 1
- Hidden Layer Activation = RELU
- Output Layer Activation = SIGMOID
- EPOCHS = 200

- ACCURACY = .7249
- LOSS = .6268

This model did not achieve the target goal.

**TRAIL 2**

I ended up changing the RELU to then use TANH to see how that would relate

- Hidden nodes layer 1 = 80
- Hidden nodes layer 2 = 30
- Output nodes = 1
- Hidden Layer Activation = TANH
- Output Layer Activation = SIGMOID
- EPOCHS = 100

- ACCURACY = .7282
- LOSS = .5604

This model did not achieve the target goal.

**TRIAL 3** 

In this trial i bucketed the INCOME_AMT and dropped the SPECIAL_CONSIDERATIONS_N variables

- Hidden nodes layer 1 = 80
-  Hidden nodes layer 2 = 30
- Output nodes = 1
- Hidden Layer Activation = RELU
- Output Layer Activation = SIGMOID
- EPOCHS = 100

- ACCURACY = .7247
- LOSS = .5624

This model did not achieve the target goal.

**TRIAL 4**

For the final trial I decided to use the same data from the model above but adding another hidden layer

- Hidden nodes layer 1 = 80
- Hidden nodes layer 2 = 50
- Hidden nodes layer 3 = 30
- Output nodes = 1
- Hidden Layer Activation = RELU
- Output Layer Activation = SIGMOID
- EPOCHS = 100

- ACCURACY = .7287
- LOSS = .5727

This model did not achieve the target goal.

**SUMMARY**

The base model was unable to reach out goal of having 75% accuracy, therefore we went to optimize the data to hopefully have a better outcome. We were unable to again achieve our goal of 75% accuracy. 

Just because the data accuracy came back below 75% doesn't mean that we can say that these charities won't be successful with more money. We could have had not taken out the proper factors or hidden layers, there are a handful of things that would have gone wrong during the application. 
