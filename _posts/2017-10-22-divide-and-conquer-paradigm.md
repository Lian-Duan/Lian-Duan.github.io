---
layout: post
title: Divide and Conquer Paradigm
---

## 1. Elements of Divide and Conquer Paradigm
- **Divide** the problem into a number of subproblems that are smaller instances of the same problem
- **Conquer** the subproblems recursively.If the subproblems are small enough, then solve them in a straightforware manner, this is the exit of the recursive computation, which is also called "bottom out"
- **Combine** the solutions to the subproblems into solution to the original problem

_I guess the most difficult part is Combine. Combine also suggests, more often, merely collecting subproblems solution does not generating solution to the orginal problem automatically, we need to combine or merge, that is, there exists some problem that is not a subproblem of the original problem_

_How can we come up with Divide and Conquer paradigm when confronted with a specific problem?_

## 2. Recurrence Equation
- Naturally, Divide and Conquer paradigm is associated with recurrence equation, which characterize the essence of Divide and Conquer paradigm when performing analysis.

+ There are three methods for solving recurrence equations:
  - substitution method: You guess a solution and substitute it for the equation and verify it's valid.
  - recursion tree:break the equation down to base case, and compute layer by layer to get a solution.
  - master theorem:$$T(n) = \mathrm{a}\!\cdot\!\mathrm{T(n/b)} + f(n)$$, according to $$\log_b a$$, we get threee possibe situations.

## 3. Examples
### 3.1 merge Sort
- Problem definition.
- Algorithm description.
- Correctness proof.
- Running time analysis.

### 3.2 maximum subarray
- Problem definition.
  Subarray is a continuous segment of some array A, $$A_ij$$ denotes the subarray of A which takes values from index i through j. All subarrays of A consists $$S = \{A_{ij} \mid 0 \le i \le j \le n\}$$
  
  Input:An array of n integers, positive and/or negative, say, $$A = (a_1, a_2,...,a_n)$$
  Output:Find a subarray $$A_{ij}\in S$$, that is, $$A_{ij} = (a_i,...,a_j)$$, $$\forall A^* \in S$$, $$\sum_{a \in A_{ij}} a \ge \sum_{b \in A^*} b$$
- Algorithm description.

Brute force algorithm, consider all the pairs(i, j),and compute the sum, thus the complexity is $$\Theta(n^2)$$

Divide and Conquer
  1.Divide the original array to two almost equal sized subarrays, left half and right half, leave middle point alone.
  2.Conquer left half and right half subarrays recursively.
  3.Combine. Find the maximum subarray that crosses the middle point. We do it like this, from the middle point which partitions the original array, compute the maximum sum and position left-wise and right-wise respectively, and merge the two parts together to form a new subarray. And now, we compare left half maximum, right half maximum, and the maximum that crosses the middle point, now we get the optimal one. 
  
- Correctness proof.
  Proof. For the base case, where the subarray have only one value, it is trivial.
         When combine, maximum subarray can have only placement, entirely left half, entirely half, crossing half, due to our algorithm, we compute all the three cases, thus we get a maximum subarray over the original array.
         By induction, we get a maximum subarray. $$\Box$$
         
- Running time analysis.
  $$\Theta(n\lg n)$$
  
### 3.3 matrix multiplication
- Problem definition.
- Algorithm description.
- Correctness proof.
- Running time analysis.

### 3.4 convex hull
- Problem definition.
- Algorithm description.
- Correctness proof.
- Running time analysis.

### 3.5 median finding
- Problem definition.
- Algorithm description.
- Correctness proof.
- Running time analysis.

### 3.6 peak finding
- Problem definition.
- Algorithm description.
- Correctness proof.
- Running time analysis.
