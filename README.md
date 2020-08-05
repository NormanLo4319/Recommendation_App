# Recommendation System
In this repository, we demonstrate some basic concepts of recommendation system and steps for building an online recommendation application. 

## Collaborative Filtering Systems:
Collaborative filtering systems recommend items based on crowdsourced information about users' preferences for items.

### Part I - Two Traditional Approaches:

#### User Based: 
User-based collaborative fitering systems are systems that recommend items based on similarity between users. Based on the attribute of the user, the systems find the similar users in the database and recommend the items based on the existing users' perference.

#### Item Based: 
Assume two items are similar when they received similar ratings from a same user. Then, we make prediction for a target user on an item by calculating weighted average of ratings on most X similar items from this user. One of the limitations is that it doesn't handle sparsity well when no one in the neighborhood rated an item that is what you are trying to predict for target user. Also, it's not computational efficient as the growth of the number of users and products.

### Part II - Machine Learning Recommendation Approaches:

#### Popularity-Based Filtering System:
Form of collaborative filtering, where items are recommended to user based on how popular those items are among other users. In most cases, the system counts the number of rating of each item in the database. The assumption is that the items that have the most number of ratings or reviews are the most popular. 

#### Correlation-Based Recommendations:
These recommenders offer a basic form of collaborative filtering because with the correlation-based recommendation systems, items are recommended based on similarities in their user's review. In another words, they take user perferences into account. These systems usually apply **Pearson's R** correlation or **Cosine Similarity** to recommend an item that is most similar to the item a user has alreayd chosen.

#### Classification-Based Collaborative Filtering Systems:
One way building a recommendation system is using classification model. It applies features of both users as well as products in order to predict whether this product liked or not by the user. One of many classification model is the **Logistic Regression**.  Based on the input, the classifier will give a binary value user may like or not, so we can make recommendation of the product to a customer. 

#### Model-Based Collaboractive Filtering Systems (Matrix Factorization):
Since sparsity and scalability are the two biggest challenges for standard Collabrative Filtering methods, there are more advanced method that decompose the original sparse matrix to low-dimensional matrices with latent factors/features and less sparsity. That is **Matrix Factorization**. To implement the matrix factorization, we demonstrate the use of **Singular Value Decomposition (SVD)**, which is a linear algebra method that can decompose a utility matrix into three compressed matrices. Model-based recommender uses these compressed matrices to make recommendations without having to refer back to the complete dataset.  

#### Content-Based Recommendation Filtering Systems:
Another popular ML algorithm of recommendation systems is content-based filtering. Content here refers to the content or attributes of the products you like. So, the idea in content-based filtering is to tag products using certain keywords, understand what the user likes, look up those keywords in the database and recommend different product with the same attributes. We  deomonstrate the use of **Nearest Neighbor** algorithm to make a prediction.

### Part III - Evaluating Recommendation Systems:
To examine which model can make the best prediction and recommendation, we need to evaluate the performance of the outcome (recommendation). For classification problem, we can look at the confusion matrix and evaluate the **Precision** and **Recall**. 


## Applying the Classifier on the Web:
Once we pick a filtering system, we can then build a web application with the selected model. When a user input the required fields, the filtering system will make a recommendation based on the feature values. We are building the web application with Python and Flask. 

### Resources: [Scikit-Learn](https://scikit-learn.org/stable/)  

Copyright © 2020 Norman Lo
