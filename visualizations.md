
# Visualizing Key Concepts in Random Variables

## 1. Uniform Distribution (PDF and CDF)

The uniform distribution is often used to represent random variables that have an equal probability over a specific range. Below is the PDF and CDF of a **Uniform(0, 1)** distribution.

![Uniform Distribution](/assets/Uniform_distribution.png)

- **PDF (Probability Density Function)**: Represents the likelihood of different outcomes.
- **CDF (Cumulative Distribution Function)**: Shows the cumulative probability up to a certain point.

---

## 2. Sum of Two Independent Uniform(0, 1) Variables

When you sum two independent **Uniform(0, 1)** random variables, the resulting distribution has a triangular shape. This is derived using **convolution** of the individual PDFs. The result is:

\[
f_Z(z) =
\begin{cases}
z & \text{if } 0 \leq z \leq 1 \\
2 - z & \text{if } 1 \leq z \leq 2
\end{cases}
\]

![Sum of Two Uniform Distributions](/assets/Sum%20of%202%20Uniform%20distributions.png)

---

## 3. Maximum of Two Uniform(0, 1) Variables

The maximum of two independent **Uniform(0, 1)** random variables follows a different distribution. The CDF of the maximum is given by:

\[
F_{\max}(z) = z^2
\]

The PDF and CDF of the maximum are plotted below:

![Maximum of Two Uniform Variables](/assets/Maximum%20of%20Two%20Uniform%20Variables.png)

---

## 4. Exponential Distribution

The **Exponential(1)** distribution is widely used in probability, especially for modeling time between events. Below is the PDF and CDF of an **Exponential(1)** distribution.

![Exponential Distribution](/assets/Exponential%20Distribution.png)

---

### Notes on Visualization:

- The PDF of the sum of independent random variables is calculated using convolution.
- Visualizing the maximum of random variables requires calculating the CDF and then differentiating to get the PDF.

[Back to Table Of Contents](tableOfContents.md)