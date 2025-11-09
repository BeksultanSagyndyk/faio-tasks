https://contest.yandex.ru/contest/69765/problems/D/


## Introduction

Clustering is the task of grouping a set of objects so that objects in the same group (called a cluster) are more similar to each other than to objects in other groups (clusters). Clustering is used in many domains, for example:

- Information retrieval: to find similar documents or web pages.
- Bioinformatics: to group genes or proteins by their functions.
- Anomaly detection: it helps identify data that do not fit the overall pattern.

Let’s consider a simple clustering example to visually demonstrate how the algorithm works on two-dimensional data:
<img width="731" height="408" alt="image" src="https://github.com/user-attachments/assets/671aad27-601d-43e6-bdaf-ecd0e9ba101d" />


This example shows how the points are divided into two clusters.

<img width="690" height="389" alt="image" src="https://github.com/user-attachments/assets/69819142-15ea-452c-bd6a-3c913db048c3" />


## K-means

We can formalize this problem. Suppose we want to find k clusters ($S_1, \dots, S_k$) such that the following objective function is minimized:

$$
L = \frac{1}{n}\sum_{j=1}^{k}\sum_{\vec{r}_i \in S_j}|\vec{r_i} - \vec{\mu_j}|^2
$$

где,
$$
\vec{\mu_j} = \frac{1}{|S_j|}\sum_{\vec{r}\in S_j}\vec{r}
$$

Finding the optimal solution to the K-means clustering problem for observations in $d$ dimensions is:

1. An NP-hard problem in a general Euclidean space (of dimension $d$) even for two clusters.
2. An NP-hard problem for a general number of clusters $k$ even in the plane.
3. For fixed $k$ and $d$ (dimensionality), the problem can be solved exactly in time $O(nd^{k+1})$, where $n$ is the number of objects to be clustered.

In practice, the following iterative algorithm is used for clustering:

1. Randomly choose $k$ centroids (a centroid is the center of a cluster).
2. For each point, find the nearest centroid and assign the point to the corresponding cluster.
3. For each cluster, compute the mean point and set it as the new centroid.
4. Repeat steps 2 and 3 until convergence.

**Example:**

Initial step: randomly choose 2 centroids.

<img width="708" height="391" alt="image" src="https://github.com/user-attachments/assets/a94fb309-e218-4c39-8126-e374ae15c630" />

first iteration of steps 2 и 3:

<img width="716" height="407" alt="image" src="https://github.com/user-attachments/assets/a8830ae9-989f-439f-8677-9a043adbde41" />


second iteration of steps 2 и 3:

<img width="705" height="400" alt="image" src="https://github.com/user-attachments/assets/a57e1bd1-0e09-4695-beef-8a4790606cf5" />


## Metric

As a baseline solution, we can solve this problem for $k=1$. In this case, the optimal cluster position will be the mean position of all points. Let us denote the loss function value in this case by $L_{baseline}$.

To evaluate how well our model performs, we can use the following formula. It yields a value from 0 to 1, where 1 is a perfect result:

$$
m  =
\begin{cases}
0  & \text{если $L \geq L_{baseline}$} \\
1 - L/L_{baseline} & \text{иначе}
\end{cases}
$$

Your task is to implement the K-means algorithm. To eliminate the randomness caused by the choice of initial centroids, you will be provided with predefined coordinates of the data points and the initial centroid positions.

You will receive 100 points if your model’s metric is at least 0.95 times our model’s metric; otherwise, you will receive 0.

The final score will be the average score across all test sets.

## Input Format

```
n
x_1 y_1
x_2 x_2
...
x_n y_n
k
cx_1 cy_1
...
cx_k cy_k
```

### Description

$n$ — number of points.

$(x_i, y_i)$ — coordinates of the $i$-th point.

$k$ — number of centroids.

$(cx_i, cy_i)$ — coordinates of the $i$-th centroid.

### Constraints

$1 < n < 1000$

$1 < k < 10$

$1 < x_i, y_i, cx_i, cy_i < 50$

### Input example
```
5

-1 1

-1 2

-2 1

1 0

2 0

2

-2 2

3 0
```

## Output format

```
cx_1 cy_1
...
cx_k cy_k
```

### Output example

```
1.5 0

-1.5 1.3
```

### Description

The final positions of your centroids after applying the K-means algorithm.
