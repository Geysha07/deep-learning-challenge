#Module 21 Challenge 

Overview of the analysis: Explain the purpose of this analysis.

Alphabet Soup, a nonprofit foundation, tasked us with finding a tool that will select applicants for funding with the best probability of success in their ventures. They have provided a CSV containing records of more than 34,000 organizations that they have funded in the past. The CSV contains the following columns:

- EIN and NAME—Identification columns
- APPLICATION_TYPE—Alphabet Soup application type
- AFFILIATION—Affiliated sector of industry
- CLASSIFICATION—Government organization classification
- USE_CASE—Use case for funding
- ORGANIZATION—Organization type
- STATUS—Active status
- INCOME_AMT—Income classification
- SPECIAL_CONSIDERATIONS—Special considerations for application
- ASK_AMT—Funding amount requested
- IS_SUCCESSFUL—Was the money used effectively

Using the information contained within the CSV, we used machine learning and neural network models to assist Alphabet Soup in selecting applicants.

Results: Using bulleted lists and images to support your answers, address the following questions:

Data Preprocessing

What variable(s) are the target(s) for your model?

The values within the "IS_SUCCESSFUL" column are the targets for the model.

What variable(s) are the features for your model?

The following columns are the features for the model.
- EIN and NAME—Identification columns
- APPLICATION_TYPE—Alphabet Soup application type
- AFFILIATION—Affiliated sector of industry
- CLASSIFICATION—Government organization classification
- USE_CASE—Use case for funding
- ORGANIZATION—Organization type
- STATUS—Active status
- INCOME_AMT—Income classification
- SPECIAL_CONSIDERATIONS—Special considerations for application
- ASK_AMT—Funding amount requested
- IS_SUCCESSFUL—Was the money used effectively

What variable(s) should be removed from the input data because they are neither targets nor features?
Compiling, Training, and Evaluating the Model

EIN and NAME are neither targets nor features, so they should be removed from the columns.

How many neurons, layers, and activation functions did you select for your neural network model, and why?

Number of neurons:
- First hidden layer: 8 neurons
- Second hidden layer: 5 neurons
- Output layer: 1 neuron

Number of layers:
- Input layer: Values from X_train
- Hidden layers: 2
- Output layer: 1

Activation functions:
- Hidden layers: ReLU
- Output layer: Sigmoid

![alt text](<Screenshot (112).png>)

I did not have a specific reason for selecting the amount of neurons and layers. I chose those to get a baseline upon which to adjust in the optimization, while avoiding overfitting. As for the activation functions, I decided to select ReLU for the hidden layers, due to its ability to handle the vanishing gradient problem and it's simplicity. As for the output layer, I selected Sigmoid since it squashes output values between 0 and 1, representing probabilities.


Were you able to achieve the target model performance?

I was not able to achieve the target model performance of 75%. In the first optimization attempt, I managed to increase slightly from 7283% in the initial model to 7324% in the first attempt, 7285% in the second attempt and 7308% in the third attempt. 

Initial Attempt
![alt text](<Screenshot (118)-1.png>)

Initial Optimization Attempt
![alt text](<Screenshot (127).png>)

Second Optimization Attempt
![alt text](<Screenshot (128).png>)

Third Optimization Attempt
![alt text](<Screenshot (129).png>)

What steps did you take in your attempts to increase model performance?

In my attempts to increase model performance, I made the following changes during optimization:

- Changed the cutoff values for application types to be replaced with other from less than 500 to less than 1065.
- Changed the cutoff values for classifications to be replaced with other from less than 1000 to less than 777.
- In my first optimization attempt, I increased the neurons in both hidden layers, from 8 and 5 to 10 and 8, for the first and second layer, respectively.
![alt text](<Screenshot (124).png>)
- In the second optimization attempt, I added a third hidden layer with 5 neurons and the tanh activation function.
![alt text](<Screenshot (125).png>)
- In my third and final optimization attempt, I eliminated the third hidden layer and increased the neurons in hidden layer one and two to 20.
![alt text](<Screenshot (126).png>)

Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.

In summary, the model was unable to meet the target accuracy of 75%, only being able to reach 73% with the optimization. My optimizations increased the accuracy, but not very much. If I didn't have time constraints, I would have added more layers with more neurons and tried different activation functions until I reached the desired accuracy percentage.
