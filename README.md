# ML-Hackathon-HDFC
ML Hackathon conducted by Hackerearth for HDFC
Problem Statement
Your task is to build a banking behavioral scorecard model for internal customers through a user's liability account and predict the credit risk. These are low transacting customers. The definition that is used for the target variable is every 30+ or X+ days delinquent twice in forward 12 months.
The implementations of the model are as follows:
•	Pre-approving customers for cross-selling other products of a bank
•	Decide the mode of treatment of customers and specify it as an input for credit underwriting
Note: You can decide the customer treatment through a graded risk profile of customers.

Approach

The problem statement is a classical Binary classification. The dataset has high dimensions and was imbalanced. In order to overcome High dimensionality, I tried three different approach- Dimensionality reduction through algorithms like PCA and Tsne and the second being Feature selection through feature importance score and the third by using built in parameters which performs L1 and L2 regularization.

L1 and L2 regularization gave a better result than Dimensionality reduction and feature selection. I used LightGBM a gradient boosting algorithm for my model building after trying various algorithms like Keras,SVM and KNN. 

The Null values in the dataset were handled with Imputation based on Median. The sole reason is that median is not affected by outliers unlike mean. 

The problem with imbalance was handled with Hyperparameter -is_unbalance. I narrowed down on is_unbalance after trying various Synthetic sampling techniques.

In order to improve accuracy, I used a very low learning rate.
 
