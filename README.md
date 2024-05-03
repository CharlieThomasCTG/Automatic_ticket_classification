# Automatic Ticket Classification

# ![image](https://github.com/charliethomasct82/Automatic_ticket_classification/assets/93368865/22e3ad74-ed43-4449-a29e-6c360e9082a1)

## Problem Statement
To Create a model that is able to classify customer complaints based on the products/services. By doing so, we can segregate these tickets into their relevant categories and, therefore, help in the quick resolution of the issue.
we will be doing topic modelling on the .json data provided by the company. Since this data is not labelled, we need to apply NMF to analyse patterns and classify tickets into the following five clusters based on their products/services:

•	Credit card / Prepaid card
•	Bank account services
•	Theft/Dispute reporting
•	Mortgages/loans
•	Others 

With the help of topic modelling, you will be able to map each ticket onto its respective department/category. We can then use this data to train any supervised model such as logistic regression, decision tree or random forest. Using this trained model, We can classify any new customer complaint support ticket into its relevant department.

# Pipelines that needs to be performed:

We need to perform the following eight major tasks to complete the assignment:
1.	Data loading
2.	Text preprocessing
3.	Exploratory data analysis (EDA)
4.	Feature extraction
5.	Topic modelling 
6.	Model building using supervised learning
7.	Model training and evaluation
8.	Model inference

# Prepare the text for topic modeling

After we have removed all the blank complaints, performed following operations:
•	Transformed  the text to lowercase
•	Removed text in square brackets
•	Removed punctuation
•	Removed words containing numbers
Once we have done these cleaning operations, we performed the following:
•	Lemmatized the texts
•	Used POS tags to get relevant words from the texts.

# Exploratory data analysis to get familiar with the data.

•	Visualised the data according to the 'Complaint' character length
•	Used a word cloud find the top 40 words by frequency among all the articles after processing the text
•	Find the top unigrams, bigrams and trigrams by frequency among all the complaints after processing the text.

# Feature Extraction

•	Converted the raw texts to a matrix of TF-IDF features
•	max_df is used for removing terms that appear too frequently, also known as "corpus-specific stop words" max_df = 0.95 means "ignore terms that appear in more than 95% of the complaints"
•	min_df is used for removing terms that appear too infrequently min_df = 2 means "ignore terms that appear in less than 2 complaints"

# Topic Modelling using NMF

Non-Negative Matrix Factorization (NMF) is an unsupervised technique so there are no labelling of topics that the model will be trained on. The way it works is that, NMF decomposes (or factorizes) high-dimensional vectors into a lower-dimensional representation. These lower-dimensional vectors are non-negative which also means their coefficients are non-negative.

In this task we performed the following:
•	Find the best number of clusters
•	Applied the best number to create word clusters
•	Inspected & validated the correction of each cluster wrt the complaints
•	Corrected the labels if needed
•	Mapped the clusters to topics/cluster names

# Manual Topic Modeling

•	We took the trial & error approach to find the best num of topics for your NMF model.
After evaluating the mapping, if the topics assigned are correct then assigned these names to the relevant topic:
•	Bank Account services
•	Credit card or prepaid card
•	Theft/Dispute Reporting
•	Mortgage/Loan
•	Others
The only parameter that is required is the number of components i.e. the number of topics we want. This is the most crucial step in the whole topic modeling process and will greatly affect how good your final topics are.

#  Applied the supervised models on the training data created. In this process, you have to do the following:
•	Created the vector counts using Count Vectoriser
•	Transformed the word vecotr to tf-idf
•	Created the train & test data using the train_test_split on the tf-idf & topics
Created and compared 3 models on the train & test data:
•	Logistic regression
•	Decision Tree
•	Random Forest

# Model Summary
![image](https://github.com/charliethomasct82/Automatic_ticket_classification/assets/93368865/000c6734-45e3-4db4-8d2b-dce10056e085)

# Model Inference
![image](https://github.com/charliethomasct82/Automatic_ticket_classification/assets/93368865/966a15da-3065-4646-9d54-b4239f6d8654)

