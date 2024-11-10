(This is generated for lectures. There might be typos and mistakes. Read with your judgment. You are welcome to send an email about them to zchen2@umassd.edu. This webpage is still under construction and will be updated occasionally.)

# All Homework Problems

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

## Section 2: Interpolation

### Homework-Problem-6
**(Analysis)** Prove that the Vandermonde matrix is invertible if the set $\{x_k\}$ consists of distinct elements, i.e.,
$$x_i \neq x_j \quad \text{for any} \quad i \neq j.$$
**Hint:** Consider the determinant of the Vandermonde matrix. There is no need to show the detailed calculation of the determinant.

### Homework-Problem-7
**(Analysis)** Show that the Lagrange interpolation can be rewritten as
$$P_n(x) = \sum_{i = 0}^n \frac{\omega_{n+1}(x)}{(x - x_i) \omega'_{n+1}(x_i)} y_i.$$

**Hint:** Check if $\frac{\omega_{n+1}(x)}{(x - x_i) \omega'_{n+1}(x_i)}$ is equal to the Lagrange basis polynomial $L_{n,i}(x)$ for all indices $i$.


### Homework-Problem-8
1. Interpolate the function $f(x) = \sin(22\pi x)$ at $22$ equally spaced nodes $\{x_1 = -1, x_2, \dots, x_{22} = 1\}$ on the interval $[-1, 1]$.
    
2. Next, generate a polluted set of values $\tilde{f}(x_i)$ of the function $f$ with a noise level of $9.5 \times 10^{-4}$, and perform polynomial interpolation on the polluted data.
    
3. Plot both interpolations (on $100$ equally spaced points over the same interval) in one figure, and comment on your observations.
    

**Hint:** Here are two ways to add noise in MATLAB:
1. `rand(22,1)` generates 22 uniformly distributed random numbers in the interval (0, 1).
2. `randn` generates random values from a standard normal distribution.  
    Be mindful of the noise level when applying these methods.

### Homework-Problem-9  
Approximate the Lebesgue constant $\Lambda_n(X_n)$ for the uniform grid of equispaced points $X_n = -1 : \frac{2}{n} : 1$.

Plot both $\Lambda_n(X_n)$ and $\frac{2^{n+1}}{n \log{n}}$​ versus $n$ in the same figure (with $n$ ranging from $1$ to $100$, using `semilogy`). Compare the two curves and comment on your observations. Do these two curves share the same increasing trend?

**Hint:** Consider how to numerically calculate the maximum of a function in a given interval, as required in the definition of the Lebesgue constant $\Lambda_n(X_n)$.

## Section 3: Differentiation

### Homework-Problem-10
**(Analysis)** For the function $f(x) = x e^x$ defined on the interval $[1, 3]$,

1. Use the centered-difference (three-point midpoint) formula with $h = 0.2$ and $h = 0.1$ to approximate $f'(2.0)$. Then, use extrapolation on these values to obtain a better approximation $N_2(0.2)$.

**Hint:** If you are unsure about the leading term in the truncation error for the centered-difference approximation of the derivative, you can use the Taylor expansion to figure it out, keeping at least two terms of the error. Then, use extrapolation based on this.

2. Show that $N_2(2h)$ gives the five-point centered-difference (midpoint) formula.

### Homework-Problem-11  
**(Analysis)** The forward-difference formula is given by
$$f'(x_0) = \frac{f(x_0 + h) - f(x_0)}{h} - \frac{f''(x_0)}{2} h - \frac{f'''(x_0)}{6} h^2 + \cdots.$$
Use extrapolation to derive a formula that approximates $f'(x_0)$ with an error of $\mathcal{O}(h^3)$. Write your formula in terms of the function’s point values and simplify your answer.


## Section 4: Integration

### Homework-Problem-12
**(Analysis)** The closed Newton-Cotes formula for n=4n = 4n=4 on the interval [−1,1][-1, 1][−1,1] is given by
$$\int_{-1}^1 f(x) \, dx \approx \omega_0 f(-1) + \omega_1 f\left(-\frac{1}{2}\right) + \omega_2 f(0) + \omega_3 f\left(\frac{1}{2}\right) + \omega_4 f(1).$$
1. What are the values of $\omega_0, \omega_1, \omega_2, \omega_3$ and $\omega_4$​?
2. Find the degree of precision of this formula.


### Homework-Problem-13
**(Analysis)** Calculate the integral
$$\int_0^1 e^x \, dx$$
using the following methods:
- Midpoint rule
- Trapezoidal rule
- Simpson’s rule
Then, apply the composite versions of these rules with 2 subintervals: $[0, 0.5]$ and $[0.5, 1]$.


### Homework-Problem-14
**(Analysis)** Consider the quadrature formula
$$Q(f) = \alpha_1 f(0) + \alpha_2 f(1) + \alpha_3 f'(0)$$
for approximating $I(f) = \int_0^1 f(x) \, dx$, where $f \in C^1([0, 1])$. Determine the coefficients $\alpha_j$​ for $j = 1, 2, 3$ such that $Q(f)$ has a degree of precision $r = 2$.


### Homework-Problem-15
**(Coding)** Apply the Composite Midpoint, Trapezoidal, and Simpson’s rules to approximate the integral $\int_0^1 |x| e^x \, dx$, and analyze their convergence as a function of the subinterval size $h$.

Determine the exact value of the integral to use as a reference for calculating the error. Plot the absolute values of the error functions for all three methods on the same figure using `loglog`, where the x-axis represents $h$ and the y-axis represents the absolute value of the error. You may use the provided `cotes.m` code to construct your subroutines.

Write your observations and comments on the convergence behavior of the methods.


### Homework-Problem-16
**(Analysis & Coding)** Consider the integral $I(f) = \int_0^1 e^x \, dx.$
Estimate the minimum number mmm of subintervals needed to compute $I(f)$ with an absolute error of at most $5 \times 10^{-4}$ using the composite trapezoidal and Simpson’s rules. In both cases, evaluate the actual absolute error obtained.


## Section 5: Approximation

### Homework-Problem-17
Given the following data:

| $x_i$ | 4.0    | 4.2    | 4.5    | 4.7    | 5.1    | 5.5    | 5.9    | 6.3    | 6.8    | 7.1    |
| ----- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| $y_i$ | 102.56 | 113.18 | 130.11 | 142.05 | 167.53 | 195.14 | 224.87 | 256.73 | 299.50 | 326.72 |
Complete the following tasks:
1. Construct the least squares polynomial of degree 1 and compute the least squares error.
2. Construct the least squares polynomial of degree 2 and compute the least squares error.
3. Construct the least squares polynomial of degree 3 and compute the least squares error.
4. Construct the least squares approximation of the form $b e^{ax}$ and compute the least squares error.
5. Construct the least squares approximation of the form $b x^a$ and compute the least squares error. (Refer to Section 8.1 in _Numerical Analysis_ by Burden and Faires, or derive the formula yourself.)


### Homework-Problem-18
**(Analysis)**
1. Use the Gram-Schmidt procedure to calculate $L_1(x)$, $L_2(x)$, and $L_3(x)$, where $\{L_0(x), L_1(x), L_2(x), L_3(x)\}$ is an orthogonal set of polynomials on $(0, \infty)$ with respect to the weight function $\omega(x) = e^{-x}$ and L0(x)≡1L_0(x) \equiv 1L0​(x)≡1. The polynomials generated from this procedure are known as the Laguerre polynomials.
    
2. Use the Laguerre polynomials calculated in part 1 to determine the least squares polynomials of degrees one, two, and three on the interval $(0, \infty)$ with respect to the weight function $\omega(x) = e^{-x}$ for the following functions. (Hint: This will require three calculations for each function, totaling 12 calculations):
    (1) $f_1(x) = x^2$; (2) $f_2(x) = e^{-x}$; (3) $f_3(x) = x^3$; (4) $f_4(x) = e^{-2x}$.

---

This version is clearer and better structured for readability and understanding.

4o

### Homework-Problem-19
Use the zeros of $\tilde{T}_3(x)$ and transformations of the given intervals to construct an interpolating polynomial of degree $2$ for the following functions. Show all steps and provide the final expressions of the quadratic polynomials.

1. $f_1(x) = \frac{1}{x}, \quad \text{on the interval } [1, 3]$
2. $f_2(x) = e^{-x}, \quad \text{on the interval } [0, 2]$
3. $f_3(x) = \frac{1}{2} \cos(x) + \frac{1}{3} \sin(2x), \quad \text{on the interval } [0, 1]$
4. $f_4(x) = x \ln(x), \quad \text{on the interval } [1, 3]$

### Homework-Problem-20
Find the general continuous least squares trigonometric polynomial $S_{n}(x)$ for the function:
$$\begin{cases} -1, & \text{if } -\pi < x < 0 \\ 1, & \text{if } 0 \leq x < \pi \end{cases}$$

**a. (Analysis)**  
Derive the formula for $S_{n}(x)$ for a general integer n≥0n \geq 0n≥0. Write the exact expressions for $S_0(x)$, $S_1(x)$, $S_2(x)$, and $S_3(x)$.

**b. (Coding)**  
Plot $f(x)$, $S_0(x)$, $S_1(x)$, $S_2(x)$, and $S_3(x)$ in the same figure. Observe and comment on your results.


### Homework-Problem-21
**a. (Analysis or Coding)**  
Determine the discrete least squares trigonometric polynomial S3(x)S_3(x)S3​(x) using $m = 4$ for the function $f(x) = e^x \cos(2x)$ on the interval $[- \pi, \pi]$. Provide the expression for $S_3(x)$.

**b. (Coding)**  
Plot the function $f(x)$ and $S_3(x)$ in the same figure. Additionally, compute the error $E(S_3)$.


### Homework-Problem-22
**(Coding)** For the function $f(x) = x$, where $x \in [-1,1]$:
1. Use `semilogy` to plot the magnitude of the Fourier coefficients and demonstrate how they decay.
2. Analyze the performance of the truncated Fourier series in approximating this function by increasing the number of terms. Comment on the effect of adding more terms.

**Instructions:**
- Print all the graphs in one figure and provide comments on your observations.
- **Hint:** Notice that the domain is not $[- \pi, \pi]$, so you will need to perform a change of variable to use the standard Fourier series formulas or provided code. For reference, consult the definition (Eq. 5) or (Eq. 7) on this Wikipedia page [https://en.wikipedia.org/wiki/Fourier_series](https://en.wikipedia.org/wiki/Fourier_series) . In the $[- \pi, \pi]$ domain, $P = 2\pi$, but for $[-1,1]$, the length $P = 2$. Modify the formulas accordingly and adjust the code as needed.

### Homework-Problem-23
**(Coding)** (Continuation of Problem 22)
Using different filters, demonstrate how the results change. Comment on your observations for each filter and compare the results across all filters.
  
## Section 6: ODEs-IVP

### Homework-Problem-24
**(a) (Analysis or Coding)**  
Use the Forward Euler method to approximate the solution for the following initial value problem (IVP):
$$y'(t) = t^{-2} \left( \sin(2t) - 2ty \right), \quad 1 \leq t \leq 2, \quad y(1) = 2, \quad \text{with } h = 0.25.$$

**(b) (Analysis)**  
The exact solution is given by
$$y(t) = \frac{1}{2t^2} \left( 4 + \cos(2) - \cos(2t) \right).$$

Derive the error bound formula for a general time step $t_i$​.  
_(Hint: What are the values of $L$ and $M$ used in the error formula?)_

**(Coding)**  
Plot the error at all time steps along with the theoretical error bound on the same figure, and compare the two. Observe the behavior of the error and comment on how closely the actual error follows the theoretical bound across the time steps.


### Homework-Problem-25
1. ** (Coding)**  
Use Taylor's method of order two and Taylor's method of order four to approximate the solution for the following initial value problem (IVP):
$$y'(t) = t^{-2} (\sin(2t) - 2ty), \quad 1 \leq t \leq 2, \quad y(1) = 2, \quad \text{with} \quad h = 0.25.$$

2. **(Coding)**  
The exact solution is:
$$y(t) = \frac{1}{2t^2} \left(4 + \cos(2) - \cos(2t)\right).$$
Plot the error at all time steps for both methods on the same figure using a `semilogy` plot, and compare the results. Observe the errors and provide your comments.

3. **(Coding)**  
Apply both Taylor methods using different values of $h$, and plot the error functions for both methods on the same figure. Use the size of $h$ as the x-axis and the corresponding absolute values of the errors as the y-axis. Use a `loglog` plot. Observe and comment on the order of convergence for each method.


### Homework-Problem-26
**(Coding)**  
Consider the irreversible chemical reaction where two molecules of solid potassium dichromate ($K_2Cr_2O_7$), two molecules of water ($H_2O$), and three atoms of solid sulfur ($S$) combine to yield three molecules of sulfur dioxide ($SO_2$), four molecules of solid potassium hydroxide ($KOH$), and two molecules of solid chromic oxide ($Cr_2O_3$). The reaction is represented symbolically by the stoichiometric equation:
$$2K_2Cr_2O_7 + 2H_2O + 3S \longrightarrow 4KOH + 2Cr_2O_3 + 3SO_2.$$

If $n_1$​ molecules of $K_2Cr_2O_7$, $n_2$​ molecules of $H_2O$, and $n_3$​ molecules of $S$ are initially available, the following differential equation describes the amount $x(t)$ of $KOH$ formed after time $t$:
$$\frac{dx}{dt} = k \left(n_1 - \frac{x}{2}\right)^2 \left(n_2 - \frac{x}{2}\right)^2 \left(n_3 - \frac{3x}{4}\right)^3,$$
where $k$ is the rate constant of the reaction.

Given that $k = 6.22 \times 10^{-19}$, $n_1 = n_2 = 2 \times 10^3$, and $n_3 = 3 \times 10^3$, use the **Runge-Kutta method of order four** to determine how many units of potassium hydroxide ($KOH$) will have been formed after 0.2 seconds.




