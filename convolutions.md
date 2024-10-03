# Understanding Convolutions

Convolution is a mathematical operation that combines two functions to produce a third function, describing how the shape of one function is modified by the other. In the context of probability distributions, convolution helps determine the distribution of the **sum** of two independent random variables.

## Convolution Formula

Given two independent random variables \( X \) and \( Y \) with PDFs \( f_X(x) \) and \( f_Y(y) \), the PDF of their sum \( Z = X + Y \) is given by the convolution of \( f_X \) and \( f_Y \):

\[
f_Z(z) = (f_X * f_Y)(z) = \int_{-\infty}^{\infty} f_X(x) f_Y(z - x) dx
\]

This integral essentially "slides" one PDF over the other, calculating how they overlap at each point.

---

## Example: Sum of Two Uniform(0, 1) Variables

Consider two independent random variables \( X \) and \( Y \), each uniformly distributed between 0 and 1. Their PDFs are:

\[
f_X(x) = 
\begin{cases}
1 & \text{if } 0 \leq x \leq 1 \\
0 & \text{otherwise}
\end{cases}
\]

To compute the PDF of \( Z = X + Y \), we convolve their PDFs:

\[
f_Z(z) = 
\begin{cases}
z & \text{if } 0 \leq z \leq 1 \\
2 - z & \text{if } 1 \leq z \leq 2
\end{cases}
\]

This results in a triangular distribution.

---

## Convolution in Practice

When summing two independent random variables, their PDFs get "smoothed out" through convolution. This is why the resulting distribution often has a different shape, typically wider and with a peak at a different location.

### Visualization Tip

Use convolution to understand how distributions change when variables are summed. The result can often be visualized as a blend of the two original distributions.

---

## Computational Tools for Convolution

While convolution can be computed by hand for simple distributions, more complex cases (like non-uniform or continuous random variables) require numerical integration. Python’s `scipy` library provides tools for performing convolutions.

For example, to compute the sum of two normal distributions:

```python
from scipy.stats import norm
import numpy as np
import matplotlib.pyplot as plt

x = np.linspace(-10, 10, 1000)
pdf_sum = np.convolve(norm.pdf(x), norm.pdf(x), mode='same')
plt.plot(x, pdf_sum)
plt.title("Convolution of Two Normal Distributions")
plt.show()

[Back to Table Of Contents](tableOfContents.md)
