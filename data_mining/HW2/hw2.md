## 1

### a)

Write the definition (formula) of the **Minkowski distance measure** and 3 special cases of it.

The Minkowski distance measure is a way to measure the length of a path between two points in a multi-dimensional space. 

$d_p(x, y) = \left( \sum_{i=1}^{n} \lvert x_i - y_i \rvert^p \right)^{1/p}, \quad p \ge 1$

The three special cases are when p equals to 1 or 2 or p -> infinity. 

When p = 1, this is called Manhattan distance.
When p = 2, this is called Euclidean distance.
When p -> infinity, this is called Chebyshev distance.

### b)

Compute the cosine similarity measurement between the following two vectors:

```
x1 = (4, 0, 1, 3, 5)
x2 = (-1, 2, 3, 0, 1)
```

```
4*-1 = -4
0 * 2 = 0
1 * 3 = 3
3 * 0 = 0
5 * 1 = 5
-4+0+3+0+5 = 4 = x_1 * x_2

|x_1| = sqrt(4^2 + 0^2 + 1^2 + 3^2 + 5^2)
|x_1| = sqrt(16 + 0 + 1 + 9 + 25)
|x_1| = sqrt(51)

|x_2| = sqrt(-1^2 + 2^2 + 3^2 + 0^2 + 1^2)
|x_2| = sqrt(1 + 4 + 9 + 0 + 1)
|x_2| = sqrt(15)

cos(theta) = 4/(sqrt(51) * sqrt(15)) = 0.1446203052
```
---

## 2

Name and explain four methods to handle noisy data.

1) Remove outliars. 
Identify the data that is far removed from the distribution of the rest of the data and remove it 
2) Clustering.
Group the similar data together. Then do analysis on each seperate cluster.
3) Average smoothing.
Replace each data point with the average of the surrounding data. This smooths out the data and makes any changes less dramatic. 
4) Binning.
Add all the data into discrete groups. Then replace the values in each bin with a the mean or median. This reduces the amount of variation in your data

---

## 3

Name two methods for handling redundant attributes in data integration and explain how to interpret their results.
(One of the methods consists of two methods, so you should explain 3 methods.)

1. Pearson's Correlation Coefficient / Covariance

Pearson's Correlation Coefficient measures the relationship between two attributes and outputs a value between -1 and +1. -1 indicates a negative correlation and +1 indicates a positive correlation. A value of 0 indicates that there is no linear relationship. It works by normalizing the covariance by the standard deviations of both attributes. Covariance measures how two variables move relative to each other but is scale dependent on its own.

2. Chi-Square Test

This measures whether or not two categorical attributes are independent. It works by comparing observed frequencies to the expected frequencies that would occur if the attributes were independent. A high chi-square value means the attributes are likely not independent, so one may be redundant.

---

## 4

### a)

Compute χ² (chi-square) calculation for the following table and justify the result.
(Numbers in parentheses are expected counts calculated based on the data distribution in the two categories.)

|                | Male      | Female    | Sum (row) |
| -------------- | --------- | --------- | --------- |
| Like cats      | 120 (182) | 310 (247) | 430       |
| Like dogs      | 330 (267) | 300 (362) | 630       |
| **Sum (col.)** | 450       | 610       | 1060      |

---

### b)

Compute the covariance matrix of the following vectors:

```
x1 = (2.5, 0.5, 2.2, 1.9, 3.1, 2.3)
x2 = (2.3, 0.8, 3.0, 2.2, 2.5, 2.8)
```
