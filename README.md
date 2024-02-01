# deep-learning-challenge

Overview

Using a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years, I created a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

Data Preprocessing

The target variable for this model is the "IS_SUCCESSFUL" column because we are attempting to predict whether or not an applicant will be successful if funded by Alphabet Soup.

The following variables are the features for my model:
APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
CLASSIFICATION—Government organization classification
USE_CASE—Use case for funding
ORGANIZATION—Organization type
STATUS—Active status
INCOME_AMT—Income classification
SPECIAL_CONSIDERATIONS—Special considerations for application
ASK_AMT—Funding amount requested

EIN and Name, the identification columns, are removed from the input data because they aren't targets or features.


Compiling, Training, and Evaluating the Model

For my initial neural network, I started with 2 hidden layers with the activation function "relu", my output layer uses sigmoid because it performs well in classification predictions.
![image](https://github.com/amandakrest/deep-learning-challenge/assets/142050568/a3aae10f-4da4-4ad1-b06c-2c950588a049)

This model is 62% accurate, which is better than a random guess but leaves room for improvement.
![image](https://github.com/amandakrest/deep-learning-challenge/assets/142050568/5f4056dc-c9e9-4e90-8df9-a1a38dda3305)

To increase model performance, I first added a hidden layer and adjusted the number of neurons to see if my original model needed more data or refining. Although this attempt yielded only slightly better results.

![image](https://github.com/amandakrest/deep-learning-challenge/assets/142050568/38edaa70-2dc4-4e6e-a9ea-e1e959a772e1)

![image](https://github.com/amandakrest/deep-learning-challenge/assets/142050568/88ed4c23-b8b2-46ce-aeed-5bafa36f20e6)

On my second attempt at optimizing my model, I included the Names of the companies that had 10 or more loans. I used the same neural network as my previous attempt in order to keep track of how each change affected the model. 
![image](https://github.com/amandakrest/deep-learning-challenge/assets/142050568/57e69f67-01b2-45eb-b793-7c4fa390d7e9)
![image](https://github.com/amandakrest/deep-learning-challenge/assets/142050568/c70c8bf0-666d-4006-9ff2-c8b511fe7e3a)
This model reached 78% accuracy. 


Summary

Overall, the deep-learning model that was most accurate, 78%, included the most data and layers out of all three attempts. This means that if Alphabet Soup were to use my model, they would accurately predict if a loan would be successful 78% of the time. While this is relatively high, I believe a different model could also solve this classification problem more accurately. My recommendation would be to add epochs or more neurons if more data is not available. But ideally, a better model may include more features such as the age and size of the company or location(suburb vs. urban). These features would give more insight into the type of situation the company is in, which often affects whether the loans are successful or not.


