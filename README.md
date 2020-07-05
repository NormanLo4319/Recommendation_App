# Recommendation_App
In this repository, we demonstrate some basic concepts and steps to build an online recommendation application. 

## Collaborative Filtering Systems:
Collaborative filtering systems recommend items based on crowdsourced information about users' preferences for items.

### Two Traditional Approaches:

#### User Based: 
Calculate the similarity between target user and all other users, select the top X similar users, and take the weighted average of ratings from these X users with similarities as weights.  Two ways to calculate similarity are **Pearson Correlation** and **Cosine Similarity**.

#### Item Based: 
Assume two items are similar when they received similar ratings from a same user. Then, we make prediction for a target user on an item by calculating weighted average of ratings on most X similar items from this user. One of the limitations is that it doesn't handle sparsity well when no one in the neighborhood rated an item that is what you are trying to predict for target user. Also, it's not computational efficient as the growth of the number of users and products.

### Machine Learning Recommendation Approaches:

#### Classification-Based Collaborative Filtering Systems:


#### Model-Based Collaboractive Filtering Systems (Matrix Factorization):
Since sparsity and scalability are the two biggest challenges for standard Collabrative Filtering methods, there are more advanced method that decompose the original sparse matrix to low-dimensional matrices with latent factors/features and less sparsity. That is **Matrix Factorization**.

**Singular Value Decomposition (SVD)**: A linear algebra method that can decompose a utility matrix into three compressed matrices. Model-based recommender uses these compressed matrices to make recommendations without having to refer back to the complete dataset.  

#### Content-Based Recommendation Filtering Systems:

#### Evaluating Recommendation Systems:
