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
    - ![InitialModelStats](https://github.com/rwoodill/deep-learning-challenge/assets/40248698/b15841fe-0e1a-4824-9e3f-c1dbb3f9ebe1)

- Were you able to achieve the target model performance?
    -  Yes, on the fourth try I was able to bring the accuracy to 0.783
    -  ![Opt4Results](https://github.com/rwoodill/deep-learning-challenge/assets/40248698/a68ba975-9a4e-41d5-82e4-fbb0c93c122f)

- What steps did you take in your attempts to increase model performance?
    - Attempt One: I added another hidden layer and changed activation type
        ![Opt1Stats](https://github.com/rwoodill/deep-learning-challenge/assets/40248698/aee60794-f36a-4af8-91da-207e8a729cf9)
        ![Opt1Results](https://github.com/rwoodill/deep-learning-challenge/assets/40248698/a9b58cc7-6881-44f5-ae3a-39ead0e96c32)
    - Attempt Two: I raised the number of epochs
        ![Opt2Stats](https://github.com/rwoodill/deep-learning-challenge/assets/40248698/2ea7a2ec-255a-44e4-8457-650324e2b0c0)
        ![Opt2Results](https://github.com/rwoodill/deep-learning-challenge/assets/40248698/095e274b-f4bc-4797-a975-0e27829bf27f)
    - Attempt Three: I increased the number of neurons per layer
        ![Opt3Stats](https://github.com/rwoodill/deep-learning-challenge/assets/40248698/c66c67bf-0bc8-484c-8470-bf94c16de419)
        ![Opt3Results](https://github.com/rwoodill/deep-learning-challenge/assets/40248698/63bafb8f-ffd8-4c17-aa3c-8f86d8b3faad)
    - Attempt Four: I changed the preprocessing of the data. Essentially, instead of simply removing the "NAME" column, I removed any "NAME" that appeared less than 10 times. Other values such as number of layers and neurons remained the same as the initial optimization attempt (Attempt One)
        ![Opt4Results](https://github.com/rwoodill/deep-learning-challenge/assets/40248698/aa5325da-e55d-4b21-a518-b85c4d0e8934)


## Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.

Overall, the model was able to achieve an accuracy of 78%. This means it will correctly classify the data 78% of the time. 

### Alternative Method

This model worked relatively well and provided close to 80% accuracy. 

However, an alternative approach could be to use the random forest model. This algorithim generates a "forest" of decision trees, combining them to produce more accurate predictions. The random forest model is well suited for classification purposes, so would be a good alternative.
