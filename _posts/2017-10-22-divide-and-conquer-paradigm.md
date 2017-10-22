---
layout: post
title: Divide and Conquer Paradigm
---

## 1. Elements of Divide and Conquer Paradigm
- **Divide** the problem into a number of subproblems that are smaller instances of the same problem
- **Conquer** the subproblems recursively.If the subproblems are small enough, then solve them in a straightforware manner, this is the exit of the recursive computation, which is also called "bottom out"
- **Combine** the solutions to the subproblems into solution to the original problem

_I guess the most difficult part is Combine. Combine also suggests, more often, merely collecting subproblems solution does not generating solution to the orginal problem automatically, we need to combine or merge_
_How can we come up with Divide and Conquer paradigm when confronted with a specific problem?_

## 2. Recurrence Equation
- Naturally, Divide and Conquer paradigm is associated with recurrence equation, which characterize the essence of Divide and Conquer paradigm when performing analysis.

+ There are three methods for solving recurrence equations:
  - substitution method: You guess a solution and substitute it for the equation and verify it's valid.
  - recursion tree:break the equation down to base case, and compute layer by layer to get a solution.
  - master theorem:T(n) = a * T(n/b) + f(n), according to \log_b a, we get threee possibe situations.

## 3. Examples
### 3.1 merge Sort
- Problem definition.
- Algorithm description.
- Correctness proof.
- Running time analysis.

### 3.2 maximum subarray
- Problem definition.
- Algorithm description.
- Correctness proof.
- Running time analysis.

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
