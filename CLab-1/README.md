# Coding Lab 1: Basic linear algebra

## Overview

In this Coding lab, you will be asked to code some linear algebra problems with NumPy. Use workflow described below for submitting your codes:
1. Fork this repository and clone your fork to your computer. 
2. Read the requirements and complete source script(s). You should define your functions in `source.py` and test them in `main.py`.
3. Commit and push.

Your coding lab **will not be marked**. It is for your practice only.

## Questions

### 1. Low-rank matrix approximation (difficulty: :star: :star:)

Given a real-valued matrix <img src="https://render.githubusercontent.com/render/math?math=A\in \Reals^{m\times n}"> and an integer <img src="https://render.githubusercontent.com/render/math?math=k\in[1, min(m,n)]">, write a function `low_rank_approx(A, k)` to compute a rank-`k` approximation `X` that minimises the Frobenius norm of <img src="https://render.githubusercontent.com/render/math?math=\|A-X\|_F">.

*I.e.* solve below math problem

<img src="https://render.githubusercontent.com/render/math?math=\arg_X\min\|A-X\|_F,s.t.  rank(X) \le k">

Hint: [Eckart–Young–Mirsky theorem](https://en.wikipedia.org/wiki/Low-rank_approximation#Proof_of_Eckart%E2%80%93Young%E2%80%93Mirsky_theorem_(for_Frobenius_norm))

### 2. Constrained linear least squares (difficulty: :star: :star: :star:)
Given two real matrices <img src="https://render.githubusercontent.com/render/math?math=A\in \Reals^{n\times n}"> and <img src="https://render.githubusercontent.com/render/math?math=B\in \Reals^{n\times n}">, write a function `constrained_LLS(A, B)` to compute a real vector <img src="https://render.githubusercontent.com/render/math?math=x\in\Reals^n"> that minimises <img src="https://render.githubusercontent.com/render/math?math=\|Ax\|_2"> subject to <img src="https://render.githubusercontent.com/render/math?math=\|Bx\|_2=1">. Out of two matrices, `A` is always full rank but `B` not necessarily so.

*I.e.* solve below math problem

<img src="https://render.githubusercontent.com/render/math?math=\arg_x\min\|Ax\|_2,s.t.\|Bx\|_2=1">

Hint: first figure out a way to solve this problem when `B` is full rank. Then generalise your solution to handle rank deficient `B` -- a common trick is to add a small constant (*e.g.* 0.000001) to its diagonal elements.

### 3. Test your codes (difficulty: :star:)

Some test cases are provided in `main.py` for your convenience. You may alternatively write your own tests in this script, however they will not be reflected in your marks.
