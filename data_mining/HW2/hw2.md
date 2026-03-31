# Logan Bolton
Data Mining - COMP 5130
## 1

### a)

Write the definition (formula) of the **Minkowski distance measure** and 3 special cases of it.

The Minkowski distance measure is a way to measure the length of a path between two points in a multi-dimensional space. 

$$
d_p(x, y) = \left( \sum_{i=1}^{n} \lvert x_i - y_i \rvert^p \right)^{1/p}, \quad p \ge 1
$$

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


```
(120-182)^2/182 = (-62)^2/182 = 3,844 / 182 ~= 21.12

(310-247)^2/247 = (63)^2/247 = 3,969 / 247 ~= 16.07

(330-267)^2/267 = (63)^2/267 = 3,969 / 267 ~= 14.87

(300-362)^2/362 = (-62)^2/362 = 3,844 / 362 ~= 10.62

21.12 + 16.07 + 14.87 + 10.62 = 62.68

Its a 2x2 table so df = (r-1)(c-1) = (2-1)(2-1) = 1

for df=1, alpha=0.05, the critical value is 3.84.
Since 62.7 > 3.84, we reject the null hypothesis that they are indepentent.
```

---

### b)

Compute the covariance matrix of the following vectors:

```
x1 = (2.5, 0.5, 2.2, 1.9, 3.1, 2.3)
x2 = (2.3, 0.8, 3.0, 2.2, 2.5, 2.8)

x1_mean = (2.5 + 0.5 + 2.2 + 1.9 + 3.1 + 2.3)/6 = 12.5/6 ~= 2.0833
x2_mean = (2.3 + 0.8 + 3.0 + 2.2 + 2.5 + 2.8)/6 = 13.6/6 ~= 2.2667

d1 = x1 - x1_mean = (0.4167, -1.5833, 0.1167, -0.1833, 1.0167, 0.2167)
d1^2 ~= 0.1736 + 2.5069 + 0.0136 + 0.0336 + 1.0336 + 0.0469

d2 = x2 - x2_mean = (0.0333, -1.4667, 0.7333, -0.0667, 0.2333, 0.5333)
d2^2 ~= 0.0011 + 2.1511 + 0.5378 + 0.0044 + 0.0544 + 0.2844

d1 * d2 ~= 0.0139 + 2.3222 + 0.0856 + 0.0122 + 0.2372 + 0.1156 ~= 2.7867

Var(x1) = 3.8083 / 5 ~= 0.7617
Var(x2) = 3.0333 / 5 ~= 0.6067
Cov(x1,x2) = 2.7867 / 5 ~= 0.5573

[[0.7617, 0.5573],
[0.5573, 0.6067]]

```
