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

 
