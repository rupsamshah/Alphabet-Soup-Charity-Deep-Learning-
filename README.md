# Alphabet Soup Charity Application Deep Learning Model

##  Overview of the analysis:
    The analysis used real world dataset which contains more than 35k organizations` data, funded by Alphabet Soup in the past. With the help of this data, the aim of the analysis is to create a deep learning neural network model to predict the success/failure of the future funds.

##  Results:
# Data Preprocessing
    * What variable(s) are the target(s) for your model?
    The column named "IS_SUCCESSFUL" is target of this model (dependent variable)

    * What variable(s) are the features for your model?
    During optimization attempts, different feature sets were used to understand their effects on the loss/accuracy.

    * What variable(s) should be removed from the input data because they are neither targets nor features?
    For all optimization attempts "EIN" variables were removed.

# Compiling, Training and Evaluating the Model
    * How many neurons, layers, and activation functions did you select for your neural network model, and why?
    Main neural network model has contained two hidden layers with 80 and 30 neurons respectively. The hidden layes used "relu" activation function while the output layer used 'sigmoid'activation function. In this analysis, the epochs number was 100.

    * Were you able to achieve the target model performance?
    The original neural network model the "EIN" and " NAME" columns were dropped and could not achieve the target model performance which was at 72%. The accuracy of this model was approximately 72% and the loss was 55%.

    * What steps did you take in your attempts to increase model performance?

    Two different optimization attempts were made to optimize the model:

    *Attempt # 1 In this attempt, couple of different alterations were made to model. Just one column was dropped ('EIN'), binning structures of 'APPLICATION_TYPE' and 'CLASSIFICATION' variables have been changed. For the "NAME" column the bin values of all names was kept to less than 100. After all these changes, accuracy level increased to 73%  while loss level decreased to 52%.

    *Attempt # 2 In this attempt also, couple of different alterations were made to model. Just one column was dropped ('EIN'), binning structures of 'APPLICATION_TYPE' and 'CLASSIFICATION' variables have been changed. For the "NAME" column the bin values of all names was kept to less than 10. By making these changes the accuracy level went up to 78% while loss level decreased to 46%.

    So, since we reached the accuracy level of 78% only 2 attempts were made for accuracy Optimization.

## Summary:
    For the original model "EIN" and "NAME" columns were eliminated . But to optimize the model and get more accuracy result just the "EIN" column was eliminated and the bin values of all names were kept to leass than 100 in first attempt, which increased the auuracy to 73% but then in second attempt mostly the code was kept same just the bin value of all names were kept to less than 10 which increase the accuracy to 78% and the loss was also decreased to 48%. Just by optimizing the original model, was able to get the accuracy of %78.