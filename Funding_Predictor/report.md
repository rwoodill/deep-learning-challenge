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
    -  Despite several tries, I was unable to raise the accuracy above 0.728
- What steps did you take in your attempts to increase model performance?
    - Attempt One: I added another hidden layer and changed activation type
    - Attempt Two: I raised the number of epochs
    - Attempt Three: I increased the number of neurons per layer

## Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.

