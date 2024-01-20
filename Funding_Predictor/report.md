# Report 
Authored by Rachel Woodill

## Overview of the analysis: Explain the purpose of this analysis.
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. 
With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

## Results: Using bulleted lists and images to support your answers, address the following questions:
### Data Preprocessing

- What variable(s) are the target(s) for your model?
    - The target variable is the "y" ("IS_SUCCESSSFUL" column).
- What variable(s) are the features for your model?
    - The features are "X" (all other columns included in dataset, i.e. "NAME", "APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION", "STATUS", "INCOME_AMT", "SPECIAL_CONSIDERATIONS", "ASK_AMT").
- What variable(s) should be removed from the input data because they are neither targets nor features?
    - The columns "EIN" and "NAME" were removed as they are neither targets nor features.

### Compiling, Training, and Evaluating the Model

- How many neurons, layers, and activation functions did you select for your neural network model, and why?
    - Initially the configuration was as follows:
        - 1st layer - 80, "relu"
        - 2nd layer - 30, "sigmoid"
        - Output layer - 1, "sigmoid"
- Were you able to achieve the target model performance?
    -  Yes, on the fourth try I was able to bring the accuracy to 0.783
- What steps did you take in your attempts to increase model performance?
    - Attempt One: I added another hidden layer and changed activation type
    - Attempt Two: I raised the number of epochs
    - Attempt Three: I increased the number of neurons per layer
    - Attempt Four: I changed the preprocessing of the data. Essentially, instead of simply removing the "NAME" column, I removed any "NAME" that appeared less than 10 times. Other values such as number of layers and neurons remained the same as the initial optimization attempt (Attempt One)

## Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.

Overall, the model was able to achieve an accuracy of 78%. This means it will correctly classify the data 78% of the time. 

### Alternative Method

This model worked relatively well and provided close to 80% accuracy. 

However, an alternative approach could be to use the random forest model. This algorithim generates a "forest" of decision trees, combining them to produce more accurate predictions. The random forest model is well suited for classification purposes, so would be a good alternative.
