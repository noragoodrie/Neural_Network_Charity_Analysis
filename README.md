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

*DATA PROCESSING*

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

