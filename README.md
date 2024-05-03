# Problem Statement
Build a model that is able to classify customer complaints based on the products/services. By doing so, we can segregate these tickets into their relevant categories and, therefore, help in the quick resolution of the issue.
we will be doing topic modelling on the .json data provided by the company. Since this data is not labelled, we need to apply NMF to analyse patterns and classify tickets into the following five clusters based on their products/services:
•	Credit card / Prepaid card
•	Bank account services
•	Theft/Dispute reporting
•	Mortgages/loans
•	Others 
With the help of topic modelling, you will be able to map each ticket onto its respective department/category. We can then use this data to train any supervised model such as logistic regression, decision tree or random forest. Using this trained model, We can classify any new customer complaint support ticket into its relevant department.
