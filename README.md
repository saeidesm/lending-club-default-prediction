# Lending Club Defaults 
 
## Project Objective
LendingClub is the world's largest peer-to-peer lending platform. It enables borrowers to create unsecured personal loans while investors can choose the loan to invest based on the information provided. 
In this project, I build machine learning models to predict the probability that a loan on LendingClub will charge off. These models could help LendingClub investors make better-informed investment decisions.

## Data Set Information
LendingClub dataset which is availble on Kaggle website.

## Data Preperation
Processing the data before trining the model, takes several steps, including: 
* Removing loan features with significant missing data, or that aren't known to investors
* Exploring, transforming, and visualizing the data
* Finding the most correlated features through correlation process 
* Creating dummy variables for categorical features 

## Data Modeling
**Sequential model** were trained on this dataset.

## Evaluation and the Results
Our model achieved a high precision of 0.88 on the test set. The F1 score is 0.93.

![confusion_matrix](https://github.com/saeidesm/lending-club-default-prediction/blob/main/confusion_matrix.jpg)


From the confusion matrix, we can see our classifier has high precision but low recall. This means the proportion of borrowers predicted to have good loan behaviors are indeed those who would fully pay the loan is high. But when the true label is charge-off, our classifier is not sensitive enough to notice that. This might be caused by the imbalanced class in the dataset. Actually, in this case, we do care more about precision as investors want to invest in those who are less likely to default.
