#Module 21 Challenge - Deep-Learning-Challenge

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

Using the information contained within the CSV, we used machine learning and neural network models to assist Alphabet Soup select applicants.

Results: Using bulleted lists and images to support your answers, address the following questions:

Data Preprocessing

What variable(s) are the target(s) for your model?

The values within the "IS_SUCCESSFUL" column are our targets for the model.

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

I used 

![alt text](<Screenshot (112).png>)


Were you able to achieve the target model performance?



What steps did you take in your attempts to increase model performance?



Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.