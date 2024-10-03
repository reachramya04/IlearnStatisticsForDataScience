
# Week 2

1. Independence of Random Variables: Explains how two or more random variables are independent, with formulas and examples.</li>
2. Functions of Random Variables: Covers transformations of random variables and how to compute their new distributions.</li>
3. Sum, Maximum, and Minimum: Illustrates how to compute the distribution of sums, maximum, and minimum of two random variables, with step-by-step solutions.

## 1. Independence of Two Random Variables

Two random variables \( X \) and \( Y \) are **independent** if the occurrence of one does not affect the probability distribution of the other. Mathematically, for all \( x \) and \( y \),

### Formula

\[
P(X = x, Y = y) = P(X = x) \cdot P(Y = y)
\]

### Explanation

Two random variables (X) and (Y) are independent if the occurrence of one does not affect the probability distribution of the other. Mathematically, (X) and (Y) are independent if for all (x) and (y): [ P(X = x \text{ and } Y = y) = P(X = x) \cdot P(Y = y) ]

### Independence of Two Random Variables Example

If \( X \) is the outcome of a fair six-sided die and \( Y \) is the outcome of a coin flip, the joint probability \( P(X = 1, Y = \text{Heads}) = P(X = 1) \cdot P(Y = \text{Heads}) = \frac{1}{6} \times \frac{1}{2} = \frac{1}{12} \).



Another Example:
Consider rolling two dice. Let (X) be the outcome of the first die and (Y) be the outcome of the second die. Since the outcome of one die does not affect the outcome of the other, (X) and (Y) are independent.

### Real-World Application

Independence is crucial in fields like finance, where the independence of stock returns can simplify the modeling of portfolio risks.


## 2. Dependence of Two Random Variables

### Dependence of Two Random Variables Explanation

Two random variables (X) and (Y) are dependent if the occurrence of one affects the probability distribution of the other. This is often measured using correlation or covariance.

### Dependence of Two Random Variables Formula

\[
   \text{Cov}(X, Y) = E[(X - E[X])(Y - E[Y])] 
\]

### Dependence of Two Random Variables Example

Consider the height and weight of individuals. These variables are dependent because taller individuals tend to weigh more.

### Dependence of Two Random Variables Real-World Application

Understanding dependence is essential in risk management, where the correlation between different assets can impact the overall risk of a portfolio.

## 3. Independence of Multiple Random Variables

Multiple random variables (X_1, X_2, \ldots, X_n) are mutually independent if the joint probability distribution is the product of their marginal distributions.

### Independence of Multiple Random Variables Formula

\[ 
  P(X_1 = x_1, X_2 = x_2, \ldots, X_n = x_n) = P(X_1 = x_1) \cdot P(X_2 = x_2) \cdot \ldots \cdot P(X_n = x_n) 
\]

### Independence of Multiple Random Variables Explanation

Multiple random variables \( X_1, X_2, \dots, X_n \) are independent if for all values of \( x_1, x_2, \dots, x_n \),

\[
P(X_1 = x_1, X_2 = x_2, \dots, X_n = x_n) = P(X_1 = x_1) \cdot P(X_2 = x_2) \cdots P(X_n = x_n)
\]

### Independence of Multiple Random Variables Example

For three independent dice rolls, the probability of getting specific outcomes \( X_1 = 1 \), \( X_2 = 3 \), and \( X_3 = 6 \) is:

\[
P(X_1 = 1, X_2 = 3, X_3 = 6) = P(X_1 = 1) \cdot P(X_2 = 3) \cdot P(X_3 = 6) = \frac{1}{6} \times \frac{1}{6} \times \frac{1}{6} = \frac{1}{216}
\]

Another Example
Consider rolling three dice. Let (X_1), (X_2), and (X_3) be the outcomes of the first, second, and third die, respectively. These variables are mutually independent.
 
### Independence of Multiple Random Variables Real-World Application

In machine learning, independence assumptions simplify the computation of joint probabilities in models like Naive Bayes.

## 4. Dependence of Multiple Random Variables

### Dependence of Multiple Random Variables Explanation

Multiple random variables (X_1, X_2, \ldots, X_n) are dependent if the occurrence of one affects the probability distribution of the others.

### Dependence of Multiple Random Variables Formula

\[
   \text{Cov}(X_i, X_j) = E[(X_i - E[X_i])(X_j - E[X_j])] 
\]

### Dependence of Multiple Random Variables Example

Consider the sales of ice cream, sunglasses, and sunscreen. These variables are dependent because they are all influenced by weather conditions.

### Dependence of Multiple Random Variables Real-World Application

In econometrics, understanding the dependence between economic indicators helps in forecasting and policy-making.

## 5. Visualizing Functions of One Random Variable

When analyzing functions of one random variable, such as \( Y = g(X) \), we are interested in how the transformation affects the distribution of \( X \).

### Visualizing Functions of One Random Variable Explanation

Visualizing functions of one random variable helps in understanding its distribution and behavior.

### Visualizing Functions of One Random Variable Example

Consider a random variable (X) representing the height of individuals. A histogram can visualize the distribution of (X).

### Visualizing Functions of One Random Variable Real-World Application

In quality control, visualizing the distribution of product dimensions helps in identifying defects.

### Visualizing Functions of One Random Variable Example

If \( X \sim \text{Uniform}(0, 1) \) and \( Y = X^2 \), the probability distribution of \( Y \) will be skewed compared to \( X \).

To **visualize** this, plot the PDF or CDF of both \( X \) and \( Y \). The shape of the distribution changes as \( X \) is squared.

--------------------------

## 6. Many-to-One Functions

A many-to-one function occurs when multiple values of \( X \) correspond to a single value of \( Y \). This complicates finding the distribution of \( Y \) because the inverse is not straightforward.

### Many-to-One Functions Example

Consider \( Y = |X| \), where \( X \sim \text{Normal}(0, 1) \). Both \( X = 1 \) and \( X = -1 \) map to \( Y = 1 \), creating a many-to-one transformation.

To compute the PDF of \( Y \), we sum the probabilities for both branches:
\[
P(Y = y) = P(X = y) + P(X = -y)
\]

## Functions of One Random Variable: Process

To solve problems involving functions of one random variable:

1. Identify the transformation \( Y = g(X) \).
2. Use the CDF or PDF transformation techniques to compute the distribution of \( Y \).
3. For continuous variables, use the formula:
\[
f_Y(y) = f_X(x) \cdot \left| \frac{dx}{dy} \right|
\]
where \( x = g^{-1}(y) \).

### Functions of One Random Variable: Process Example

If \( X \sim \text{Exponential}(\lambda) \) and \( Y = X^2 \), the PDF of \( Y \) is derived by transforming the exponential distribution.

## Introduction to Functions of Two Random Variables

Given two random variables \( X \) and \( Y \), a new variable \( Z \) can be formed as a function of both, i.e., \( Z = g(X, Y) \).

### Introduction to Functions of Two Random Variables Example

If \( X \sim \text{Uniform}(0, 1) \) and \( Y \sim \text{Uniform}(0, 1) \), we can define \( Z = X + Y \). The distribution of \( Z \) will depend on the joint behavior of \( X \) and \( Y \).

## Visualizing Functions of Two Random Variables

To visualize functions of two random variables, we can plot the joint distribution and the transformation surface. For example, for \( Z = X + Y \), plot the joint PDF of \( X \) and \( Y \), and then the resulting distribution of \( Z \).

### Visualizing Functions of Two Random Variables Example

For independent uniform random variables \( X \) and \( Y \), the sum \( Z = X + Y \) has a triangular distribution, which can be plotted as a 3D surface or a contour plot.

## Sum of Two Random Variables

The sum of two independent random variables \( X \) and \( Y \) has a distribution given by the **convolution** of their individual PDFs:
\[
f_Z(z) = (f_X * f_Y)(z) = \int_{-\infty}^{\infty} f_X(x) f_Y(z - x) dx
\]

### Sum of Two Random Variables Example

If \( X \sim \text{Uniform}(0, 1) \) and \( Y \sim \text{Uniform}(0, 1) \), their sum \( Z = X + Y \) has the PDF:
\[
f_Z(z) =
\begin{cases}
z & \text{if } 0 \leq z \leq 1 \\
2 - z & \text{if } 1 \leq z \leq 2
\end{cases}
\]

## Maximum of Two Random Variables

For independent random variables \( X \) and \( Y \), the maximum \( Z = \max(X, Y) \) is computed using the **CDF**:
\[
F_Z(z) = P(\max(X, Y) \leq z) = P(X \leq z) P(Y \leq z)
\]
\[
f_Z(z) = \frac{d}{dz} F_Z(z)
\]

### Maximum of Two Random Variables Example

For \( X \sim \text{Uniform}(0, 1) \) and \( Y \sim \text{Uniform}(0, 1) \), the CDF of \( Z = \max(X, Y) \) is:
\[
F_Z(z) = z^2
\]

The PDF is:
\[
f_Z(z) = 2z
\]

## Functions of Two Random Variables: Process

To find the distribution of a function \( Z = g(X, Y) \):

1. Use joint distribution techniques (e.g., convolution for sums).
2. Compute the CDF or PDF through appropriate transformations.

## Minimum and Maximum of Two Random Variables

The minimum and maximum of two random variables \( X \) and \( Y \) can be computed using their CDFs:

- **Minimum** \( Z = \min(X, Y) \):
  \[
  F_Z(z) = 1 - (1 - F_X(z))(1 - F_Y(z))
  \]

- **Maximum** \( Z = \max(X, Y) \):
  \[
  F_Z(z) = F_X(z) F_Y(z)
  \]

### Minimum and Maximum of Two Random Variables Example

For independent \( X, Y \sim \text{Uniform}(0, 1) \),
\[
F_{\min}(z) = 1 - (1 - z)^2 = 2z - z^2
\]
\[
F_{\max}(z) = z^2
\]

=========================================================










6. Many-to-One Functions
Explanation
A many-to-one function maps multiple inputs to a single output.

Example
Consider the function (f(x) = x^2). Both (x = 2) and (x = -2) map to (f(x) = 4).

Real-World Application
In cryptography, many-to-one functions are used in hash functions to map data of arbitrary size to fixed-size values.

7. Examples of Functions of One Random Variable
Explanation
Examples help in understanding the application of functions of one random variable.

Example
Consider the function (f(x) = \sin(x)). If (X) is a random variable representing angles, (f(X)) represents the sine of those angles.

Real-World Application
In signal processing, functions of random variables are used to model noise and filter signals.

8. Introduction to Functions of Two Random Variables
Explanation
Functions of two random variables involve operations on pairs of random variables.

Example
Consider the function (f(X, Y) = X + Y). If (X) and (Y) are random variables representing the outcomes of two dice, (f(X, Y)) represents their sum.

Real-World Application
In finance, functions of two random variables are used to model the joint behavior of asset returns.

9. Visualizing Functions of Two Random Variables
Explanation
Visualizing functions of two random variables helps in understanding their joint distribution.

Example
Consider a 3D plot of the joint distribution of two random variables (X) and (Y).

Real-World Application
In meteorology, visualizing the joint distribution of temperature and humidity helps in weather forecasting.

10. Sum of Two Random Variables
Explanation
The sum of two random variables (X) and (Y) is another random variable (Z = X + Y).

Formula
[ E[Z] = E[X] + E[Y] ] [ \text{Var}(Z) = \text{Var}(X) + \text{Var}(Y) + 2\text{Cov}(X, Y) ]

Example
Consider rolling two dice. The sum of the outcomes is a random variable representing the total score.

Real-World Application
In queuing theory, the sum of service times of customers represents the total time spent in the system.

11. Maximum of Two Random Variables
Explanation
The maximum of two random variables (X) and (Y) is another random variable (Z = \max(X, Y)).

Example
Consider the maximum temperature recorded in two different cities on a given day.

Real-World Application
In reliability engineering, the maximum of the lifetimes of components determines the system’s lifetime.

12. Functions of Two Random Variables
Explanation
Functions of two random variables involve operations on pairs of random variables.

Example
Consider the function (f(X, Y) = X \cdot Y). If (X) and (Y) are random variables representing the lengths of two sides of a rectangle, (f(X, Y)) represents the area.

Real-World Application
In economics, functions of two random variables are used to model the interaction between supply and demand.

13. Minimum and Maximum of Two Random Variables
Explanation
The minimum and maximum of two random variables (X) and (Y) are new random variables (Z_{\min} = \min(X, Y)) and (Z_{\max} = \max(X, Y)).

Example
Consider the minimum and maximum scores of two students in an exam.

Real-World Application
In project management, the minimum and maximum of task durations determine the project timeline.


[Back to Table Of Contents](tableOfContents.md)


