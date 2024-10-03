
# Explanation of the Topics

1. Independence of Random Variables: Explains how two or more random variables are independent, with formulas and examples.</li>
2. Functions of Random Variables: Covers transformations of random variables and how to compute their new distributions.</li>
3. Sum, Maximum, and Minimum: Illustrates how to compute the distribution of sums, maximum, and minimum of two random variables, with step-by-step solutions.

## Independence of Two Random Variables

Two random variables \( X \) and \( Y \) are **independent** if the occurrence of one does not affect the probability distribution of the other. Mathematically, for all \( x \) and \( y \),

\[
P(X = x, Y = y) = P(X = x) \cdot P(Y = y)
\]

### Independence of Two Random Variables Example

If \( X \) is the outcome of a fair six-sided die and \( Y \) is the outcome of a coin flip, the joint probability \( P(X = 1, Y = \text{Heads}) = P(X = 1) \cdot P(Y = \text{Heads}) = \frac{1}{6} \times \frac{1}{2} = \frac{1}{12} \).

## Independence of Multiple Random Variables

Multiple random variables \( X_1, X_2, \dots, X_n \) are independent if for all values of \( x_1, x_2, \dots, x_n \),

\[
P(X_1 = x_1, X_2 = x_2, \dots, X_n = x_n) = P(X_1 = x_1) \cdot P(X_2 = x_2) \cdots P(X_n = x_n)
\]

### Independence of Multiple Random Variables Example

For three independent dice rolls, the probability of getting specific outcomes \( X_1 = 1 \), \( X_2 = 3 \), and \( X_3 = 6 \) is:

\[
P(X_1 = 1, X_2 = 3, X_3 = 6) = P(X_1 = 1) \cdot P(X_2 = 3) \cdot P(X_3 = 6) = \frac{1}{6} \times \frac{1}{6} \times \frac{1}{6} = \frac{1}{216}
\]

## Visualizing Functions of One Random Variable

When analyzing functions of one random variable, such as \( Y = g(X) \), we are interested in how the transformation affects the distribution of \( X \).

### Visualizing Functions of One Random Variable Example

If \( X \sim \text{Uniform}(0, 1) \) and \( Y = X^2 \), the probability distribution of \( Y \) will be skewed compared to \( X \).

To **visualize** this, plot the PDF or CDF of both \( X \) and \( Y \). The shape of the distribution changes as \( X \) is squared.

## Many-to-One Functions

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





