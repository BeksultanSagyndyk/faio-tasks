# A. Choosing rocket
https://contest.yandex.ru/contest/71291/problems/A/

Time limit: 1 second
Memory limit: 64 MB
Input: standard input or input.txt
Output: standard output or output.txt

The team is preparing to fly on a business trip to a space station. They need to choose k rocket components out of n. In how many ways can they do this? The order of selection does not matter.

Two natural numbers n and k are given. Output the answer to the problem.

# B. Expected Value
https://contest.yandex.ru/contest/71291/problems/B/

A point M is chosen uniformly at random inside an equilateral triangle ABC. The area of the triangle is 1.
Find the expected value of the area of triangle ABM.

Output the answer in the form a/b.

# C. Flight Speed

https://contest.yandex.ru/contest/71291/problems/C/

# C. Flight Speed

**Time limit:** 1 second  
**Memory limit:** 64 MB  
**Input:** standard input or `input.txt`  
**Output:** standard output or `output.txt`

Arman and his assistants are flying from Earth to a space station to repair the gravity matrix.  
The rocket’s time–distance graph (time `x` in hours since launch, distance `y` in kilometers from Earth) follows a parabola:
\[
y = a x^2 + b x + c.
\]
They want to know the rocket’s speed exactly `d` hours after launch.

**Input**  
Real numbers `a`, `b`, `c`, and `d` on separate lines.  
Constraints: \(0 < a, b, c, d < 1000\).

**Output**  
Print the answer to the problem.

**Sample Input**

10 4.65116 7.178 12

**Sample Output**

244.65116

# D. Flight Speed 2: Data Lost
https://contest.yandex.ru/contest/71291/problems/D/

**Time limit:** 1 second  
**Memory limit:** 64 MB  
**Input:** standard input or `input.txt`  
**Output:** standard output or `output.txt`

A team of space engineers flew to the station, but debris altered their speed at the very start, breaking the plan from the previous task. It is known that the new time–distance graph is also a parabola. Runi managed to record data for their ship at three points before the sensor failed. They hope this is enough to recover the graph.

Find the real numbers `a`, `b`, `c` of the parabola
\[
y = a x^2 + b x + c
\]
given that it passes through three points with real coordinates:

- The first point is \((x_1, y_1)\).
- The second point is **to the left of the first point by** \(x_2\) and **above the third point by** \(y_2\).
- The third point is \((x_3, y_3)\).

Thus, the second point has coordinates \((x_1 - x_2,\; y_3 + y_2)\).

All mentioned variables are greater than \(-1000\) and less than \(1000\).

**Input**  
Six real numbers on one line separated by spaces:  
`x1 y1 x2 y2 x3 y3`

**Output**  
Print the three real numbers `a b c` separated by spaces.

# E. Ray is behaving bad
https://contest.yandex.ru/contest/71291/problems/E/

**Time limit:** 1 second  
**Memory limit:** 64 MB  
**Input:** standard input or `input.txt`  
**Output:** standard output or `output.txt`

Ray is on the first floor of a space station consisting of a single point.  
The **second** and **third** floors are regular pentagons with **only side edges** (no diagonals).

- The point on the **first floor** is connected by stairs to **each** vertex on the **second floor**.  
- Each vertex on the **second floor** is connected by stairs to its **two neighboring** vertices (adjacent along the pentagon).  
- Each vertex on the **third floor** is connected to **two** stairs coming from the **second floor**.  
- The **fourth floor** is a single point, and **each** vertex on the **third floor** is connected by a staircase to the **fourth-floor** point.

Ray moves continuously from vertex to vertex. Upon reaching any vertex, he chooses **uniformly at random** among all available outgoing stairs and traverses one staircase in **one minute**.

**Task**  
What is the probability that Ray reaches the fourth floor in **3 minutes**?  
Print the answer as a **decimal fraction** (floating-point number).

**Input**  
No input.

**Output**  
Print the probability as a floating-point number.

# F. Gravitational Matrix

https://contest.yandex.ru/contest/71291/problems/F/

**Time limit:** 1 second  
**Memory limit:** 64 MB  
**Input:** standard input or `input.txt`  
**Output:** standard output or `output.txt`

Arman, the **Gravitational Architect**, and Roony, the **Spatial Stabilization Technician**, need to compute the product of two matrices representing gravitational parameters on the FAIO space station.

Given two matrices:
- The first matrix has size `a × b`.
- The second matrix has size `b × c`.

Compute their product (first multiplied by second) and output the resulting `a × c` matrix.

---

## Input
- Three natural numbers `a`, `b`, `c` — the matrix dimensions.  
- Then follow `a` lines, each containing `b` real numbers — the first matrix.  
- Then follow `b` lines, each containing `c` real numbers — the second matrix.

**Constraints**
- \(1 \le a, b, c \le 300\).
- Matrix multiplication is valid since the first has `b` columns and the second has `b` rows.
- All matrix entries are real numbers.

## Output
Print the product matrix as `a` lines, each containing `c` real numbers separated by spaces.

# G. Into Space

https://contest.yandex.ru/contest/71291/problems/G/

**Time limit:** 1 second  
**Memory limit:** 64 MB  
**Input:** standard input or `input.txt`  
**Output:** standard output or `output.txt`

The team needs to place **4 magnets** in a single plane. For them to operate smoothly, **all pairwise distances** between the magnets must be natural numbers \(a, b, c, d, e, f\) (in meters). They are unsure whether this is possible—help them decide.

**Input**  
One line with six natural numbers (in meters):  
`a b c d e f`

**Output**  
If such a placement is possible, print `"yes"`. Otherwise, print `"no"`.

# H. Meteorites with Gold

https://contest.yandex.ru/contest/71291/problems/H/

**Time limit:** 1 second  
**Memory limit:** 64 MB  
**Input:** standard input or `input.txt`  
**Output:** standard output or `output.txt`

The gravitational matrix is working perfectly! Every minute, it pulls **one meteorite** toward the station for research and for finding gold. There are `x` meteorites around the station in total, and exactly `g` of them contain gold. Meteorites are pulled in one by one. What is the **expected number of minutes** until a meteorite **with gold** is pulled in?

**Input**  
Two natural numbers `x` and `g` separated by a space.  
Constraints: `0 < g <= x < 100000`.

**Output**  
Print the answer as a **decimal fraction** (floating-point number).

**Sample Input**

1 1

**Sample Output**

1

# I. Ray Is Misbehaving 2: Interference

https://contest.yandex.ru/contest/71291/problems/I/

**Time limit:** 1 second  
**Memory limit:** 64 MB  
**Input:** standard input or `input.txt`  
**Output:** standard output or `output.txt`

After being pulled in, meteorites fly farther into space approximately along a **single straight line**. However, as Ray ran through the corridors, he occasionally bumped the gravitational matrix, causing some meteorites to deviate from the common line by **more than 40%**.  
You are given the meteorite coordinates; each meteorite has real coordinates \((x, y, z)\), and for **all** meteorites, \(z = 1\).

**Input**  
- An integer `n` — the number of meteorites.  
- Then follow `n` lines, each containing **four real numbers** separated by spaces:  
  `id x y z`  
  where `id` is the meteorite number, and `(x, y, z)` are its coordinates.

**Output**  
Print the **ids** of the meteorites that deviated (by more than 40%) **in one line**, separated by spaces.

# J. Dividing the Stars
https://contest.yandex.ru/contest/71291/problems/J/

**Time limit:** 1 second  
**Memory limit:** 64 MB  
**Input:** standard input or `input.txt`  
**Output:** standard output or `output.txt`

On a plane, there are marked neutron stars and giant stars. No three stars lie on the same straight line.

You are given an integer `n`.  
The next `n` lines contain the coordinates of the neutron stars (two real numbers per line).  
The following `n` lines contain the coordinates of the giant stars (two real numbers per line).

Find a line of the form
\[
y = a x + b
\]
that passes through **one neutron star** and **one giant star** such that, in **one** of the open half-planes determined by this line, the numbers of neutron stars and giant stars are **equal**. It is guaranteed that a solution of the form \(y = ax + b\) exists.

**Input**  
- `n`  
- `n` lines: `x y` for neutron stars (real numbers)  
- `n` lines: `x y` for giant stars (real numbers)

**Output**  
Print `a` and `b` separated by a space.

**Constraints**  
- \(1 < n < 10^5\)  
- All coordinates are real numbers with \(0 < x,y < 10^6\)  
- No three stars are collinear.
