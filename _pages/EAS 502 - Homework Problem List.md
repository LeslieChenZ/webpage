---
permalink: /teaching/EAS502Hws
title: ""
last_modified_at: 2024-11-10
categories:
  - Pages
tags:
  - teaching
  - links
---

# EAS 502 - All Homework Problems
(This is generated for lectures. There might be typos and mistakes. Read with your judgment. You are welcome to send an email about them to **_zchen2@umassd.edu_**. This webpage is still under construction and will be updated occasionally.)

**Last updated on 2024-11-10**

## Table of Contents

- Section 1: Root Finding
    - [Homework-Problem-1](#homework-problem-1)
    - [Homework-Problem-2](#homework-problem-2)
    - [Homework-Problem-3](#homework-problem-3)
    - [Homework-Problem-4](#homework-problem-4)
    - [Homework-Problem-5](#homework-problem-5)
- Section 2: Interpolation
    - [Homework-Problem-6](#homework-problem-6)
    - [Homework-Problem-7](#homework-problem-7)
    - [Homework-Problem-8](#homework-problem-8)
    - [Homework-Problem-9](#homework-problem-9)
- Section 3: Differentiation
    - [Homework-Problem-10](#homework-problem-10)
    - [Homework-Problem-11](#homework-problem-11)
- Section 4: Integration
    - [Homework-Problem-12](#homework-problem-12)
    - [Homework-Problem-13](#homework-problem-13)
    - [Homework-Problem-14](#homework-problem-14)
    - [Homework-Problem-15](#homework-problem-15)
    - [Homework-Problem-16](#homework-problem-16)
- Section 5: Approximation
    - [Homework-Problem-17](#homework-problem-17)
    - [Homework-Problem-18](#homework-problem-18)
    - [Homework-Problem-19](#homework-problem-19)
    - [Homework-Problem-20](#homework-problem-20)
    - [Homework-Problem-21](#homework-problem-21)
    - [Homework-Problem-22](#homework-problem-22)
    - [Homework-Problem-23](#homework-problem-23)
- Section 6: ODEs-IVP
    - [Homework-Problem-24](#homework-problem-24)
    - [Homework-Problem-25](#homework-problem-25)
    - [Homework-Problem-26](#homework-problem-26)

---
## Section 1: Root Finding

### Homework-Problem-1

In this exercise, you will implement your own fixed-point iteration algorithm and apply it to the following two functions separately. After implementing the algorithm, answer the questions listed below for each function.
1. $g_1(x) = x - x^5$
2. $g_2(x) = x + x^5$
### Questions:

**Q1:** What is the fixed point of each function? Explain why.

**Q2:** How is the fixed-point iteration applied to move from the current iteration $p_n$​ to the next iteration $p_{n+1}$​? Provide the formula used in this iteration process.

**Q3:** Does the fixed-point iteration provide a good approximation of the fixed point?
- If yes, discuss how to choose a suitable range for the search and what makes a good initial guess.
- If not, explain why not.  
In each case, use the theory covered in class to justify your reasoning.

**Q4:** Observe and discuss the convergence speed of the iteration.
**Hint:** The results of the two functions might be very different.



### Homework-Problem-2

1. Implement your own subroutines/functions for the five root-finding numerical methods:
    - Bisection method
    - Newton's method
    - Chord method
    - Secant method
    - Method of false position
     
2. Create and test a subroutine/function that selects a root-finding method based on user input. The function should follow this structure:
    `[...] = myfzeros(...., method);`
    where:
    - `'b'` corresponds to the Bisection method
    - `'n'` corresponds to Newton's method
    - `'c'` corresponds to the Chord method
    - `'s'` corresponds to the Secant method
    - `'f'` corresponds to the Method of False Position
     
3. Apply your implementations to find the root of ==a function for which you know the exact root==.
    - Plot the convergence error histories for all five methods on the same figure. (**Hint:** The error is the difference between the exact root and the iterates/approximations.)
    - Comment on and compare the convergence speed (also referred to as "convergence order") of the five methods. It is recommended to plot the convergence speeds in a single figure for comparison.
**Hint:** In the error history plot, use the iteration number $n$ for the x-axis and the logarithm of the absolute errors of the approximations for the y-axis. You can refer to "Test_zero_convergence" for demonstration.

### Homework-Problem-3
**(Analysis)** Suppose $p$ is a zero of multiplicity mmm of the function $f(x)$. The iteration function for Newton's method applied to $f(x) = 0$ is given by $g(x) = x - \frac{f(x)}{f'(x)}$. Prove that $$g'(p) = 1 - \frac{1}{m}.$$

### Homework-Problem-4
**(Analysis)** Consider the function $f(x) = (x - p)^m q(x)$, which has a zero of multiplicity $m$ at $p$. Apply Newton's method to the function $\mu(x) = \frac{f(x)}{f'(x)}$​.

1. What is the convergence order of Newton's method for $\mu(x)$?
2. Why? Justify/prove your conclusion.

**Hint:** Think about the formula for $\mu(x)$. Is ppp a zero of $\mu(x)$? If so, what is its multiplicity? The conclusion from Problem 3 might be helpful here. Consider the iteration function of Newton's method applied to $\mu(x)$, and use the theorems learned in class to help you reach and justify your conclusion.

### Homework-Problem-5
Let $f(x) = e^x - x - 1$.

1. **[Coding]** Apply Newton's method to $f(x)$ with the initial guess $p_0 = 1$. Show that the method converges to the root $p = 0$, but not quadratically. Use your code to calculate the first $20$ iterates and compute the numerical orders of convergence. If additional iterations are needed, feel free to do so, but make sure to clearly state the number of iterations used. Comment on your observations.
    
2. **[Coding]** Repeat the process for the function $\mu(x) = \frac{f(x)}{f'(x)}$.
    
3. **[Analysis]** Use theorems (either from class or conclusions drawn from previous homework) to prove the observations regarding the numerical orders of convergence made in parts 1 and 2.


