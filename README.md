# Netflix Prize

## Introduction

The Netflix Prize was an open competition held from 2006 to 2009 for the best collaborative filtering algorithm to predict user ratings for films. The prediction was based on previous ratings from users of Netflix's movies without other information about users or films.
 
It rewarded the top team with an incremental 10% improvement on their existing CineMatch algorithm with 1M dollars. The winning team, BellKor, led by AT&T Research engineers, ended up winning the prize by beating Netflix's baseline.
 
The goal of this project is to build a Recommendation System to beat Netflix and BellKor's baselines using sparse methods for recommendation systems.

## Dataset 

Here are summary statistics about the dataset:

- Ratings from 1 to 5
- 17K movies
- 99M ratings
- 480K viewers
- 206 movies seen on average
- Average rating of 3.6
- 9B entries but only 99M are non-zero
- Stored in compressed sparse row (CSR) matrix format using SciPy
- Requires only 700MB of memory instead of 34GB assuming 32-bit integer representation

## Algorithms

We implement 3 different algorithms for this problem which are well suited for recommendation systems.

### The SVD Algorithm

The SVD algorithm consists of decomposing the user-item interaction matrix into the product of two lower-dimensionality rectangular matrices and then performing their product to predict the values of non-empty cells in the user-movie interaction matrix.

### The SVD++ Algorithm

The SVD++ algorithm is an extension of the SVD that uses implicit ratings (the fact that a user rated a movie, regardless of the rating).

### The KNN Algorithm

The KNN algorithm is a KNN based approach that looks at ratings of neighbors to make a prediction. We use cosine similarity for similarity which is efficient with sparse vectors.

## Results 

We run a 3-fold Grid Search Cross Validation and tune the learning rate and regularization hyperparameters of SVD and SVD++:

## Future Work

- Use ensemble models to improve on the current predictions by learning model weights
- Use a larger cluster to have a bigger Grid Search for SVD++

## References

[1] Yehuda Koren, Robert Bell, and Chris Volinsky. Matrix factorization techniques for recommender systems. Computer, 42(8):30–37, 2009.
 
[2] Ramni Harbir Singh, Sargam Maurya, Tanisha Tripathi, Tushar Narula, and Gaurav Srivastav. Movie recommendation system using cosine similarity and knn. International Journal of Engineering and Advanced Technology, 9(5):556–559, 2020.


