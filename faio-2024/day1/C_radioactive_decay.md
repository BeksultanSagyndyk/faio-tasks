https://contest.yandex.ru/contest/69765/problems/C/

## Введение
In physics, it is known that radioactive substances lose half of their activity or mass every T_0 seconds, which is described by the following equation:

$$m(t) = m_0 \left(\frac{1}{2}\right)^{t / T_0}$$

You are given experimental results as n pairs of values (t, m(t)). Your task is to determine the half-life T_0.

<img width="646" height="466" alt="image" src="https://github.com/user-attachments/assets/d68b70c0-e364-43d4-9759-b615a3f7feb3" />


For this task, you can use various heuristic methods or the classical linear regression method, after first transforming the data for convenience.

## Linear Regression

Let’s consider a dataset $\{(x_i, y_i)\}_{i=0}^n$ that exhibits a linear relationship. We can model this relationship using the linear function $f(x) = ax + b$, where $a$ and $b$ are the model parameters representing the slope and intercept, respectively.

<img width="996" height="665" alt="image" src="https://github.com/user-attachments/assets/d63a3ae5-1cbb-45b5-b940-ac9b9c8d846a" />


The parameters of the resulting linear function can be determined by minimizing the mean squared deviation of each point from the line:

$$L(a, b) = \frac{1}{n}\sum_{i=0}^n\left(f(x_i) - y_i\right)^2 = \frac{1}{n}\sum_{i=0}^n\left(ax_i+b - y_i\right)^2 \rightarrow \min$$

By solving the equations $\frac{\partial}{\partial a}L(a, b) = 0$ and $\frac{\partial}{\partial b}L(a, b) = 0$, one can analytically determine the values of $a$ and $b$.

## Evaluation Criteria

If your prediction is within 1% of the correct answer, you will receive 100 points. Otherwise, the result will be 0.
The final score will be calculated as the average of the scores across all test sets.

## Input Format

```
n
m_1 t_1
m_2 t_2
...
m_n t_n
```

### Description

- $n$: number of measurements.
- $m_i$: mass of the radioactive element (real number) at time $t_i$ (real number).

### Constraints

- $1 < n \le 1000$
- $1 < m_i \le 10000$
- $1 \le t_i \le 5000$

### Input example

```
5
1000 0
500 10
250 20
125 30
62.5 40.0
```

In this example:

There are 5 measurements. The initial mass is 1000. The half-life is 10 seconds.

## Output Format
$T_0$

### Sample Output

```
10.01
```

### Подсказка
В решении этой задачи может оказаться полезным использовать натуральный логарифм.

```python
from math import log
```
