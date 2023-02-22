# Neural_Network_Charity_Analysis

## Overview of the analysis
We are aiming to predict whether applicants will be successful if funded by Alphabet soup.
We use a dataset of 34,000 organization who received funding from Alphabet Soup over the years. 

We have 3 steps to our analysis before ending with the summary analysis;
Step 1: Preprocessing Data for a Neural Network Model
Step 2: Compile, Train, and Evaluate the Model
Step 3: Optimize the Model


## Results: Using bulleted lists and images to support your answers, address the following questions.


### Data Preprocessing
- What variable(s) are considered the target(s) for your model?
Checking to see if the target is marked as successful in the DataFrame, indicating that it has been successfully funded by AlphabetSoup.

- What variable(s) are considered to be the features for your model?
The IS_SUCCESSFUL column is the feature chosen for this dataset.

- What variable(s) are neither targets nor features, and should be removed from the input data?
The EIN and NAME columns will not increase the accuracy of the model and can be removed to improve code efficiency.

### Compiling, Training, and Evaluating the Model
- How many neurons, layers, and activation functions did you select for your neural network model, and why?
In the optimized model, layer 1 started with 120 neurons with a relu activation. For layer 2, it dropped to 80 neurons and continued with the relu activation. From there, the sigmoid activation seemed to be the better fit for layers 3 (40 neurons) and layer 4 (20 neurons).
![image](https://user-images.githubusercontent.com/75656368/220505068-09f14185-082a-4bc8-a7e3-0918f20d8e0e.png)

- Were you able to achieve the target model performance?
The target for the model was 75%, but the best the model could produce was 72.7%.

- What steps did you take to try and increase model performance?
Columns were reviewed and the STATUS and SPECIAL_CONSIDERATIONS columns were dropped as well as increasing the number of neurons and layers. Other activations were tried such as tanh, but the range that model produced went from 40% to 68% accuracy. The linear activation produced the worst accuracy, around 28%. The relu activation at the early layers and sigmoid activation at the latter layers gave the best results.
![image](https://user-images.githubusercontent.com/75656368/220505143-6e24a08d-ba0e-47b5-a7dc-fc23d203622c.png)
![image](https://user-images.githubusercontent.com/75656368/220505106-76f51d88-85f8-4c27-8dcd-213df6d2cd0c.png)


##Summary & recommendation
The relu and sigmoid activations yielded a 72.7% accuracy, which is the best the model could produce using various number of neurons and layers. The next step should be to try the random forest classifier as it is less influenced by outliers.
