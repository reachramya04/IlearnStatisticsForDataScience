
# Understanding and Visualizing Random Variables and Their Functions

## Introduction

In the realm of probability theory, random variables are essential tools to model uncertain quantities. When we study the relationship between multiple random variables, we delve into concepts like independence and dependence. This study material aims to provide a comprehensive understanding of these concepts, along with their visualizations and applications.

The concept of independent random variables is very similar to independent events. Remember, two events A and B
 are independent if we have 

\[
    P(A,B)=P(A)P(B)
\]   

 remember comma means "and" , i.e.,

\[
    P(A,B)=P(A and B)=P(A∩B)
\]

Similarly, we have the following definition for independent discrete random variables.

![alt text](/assets/independentRV.png)

Intuitively, two random variables X and Y are independent if knowing the value of one of them does not change the probabilities for the other one. In other words, if X and Y are independent, we can write 
\[
    P(Y=y|X=x)=P(Y=y), for all x,y
\]
Similar to independent events, it is sometimes easy to argue that two random variables are independent simply because they do not have any physical interactions with each other. Here is a simple example: I toss a coin 2N times. Let X be the number of heads that I observe in the first N coin tosses and let Y be the number of heads that I observe in the second N coin tosses. Since X and Y are the result of independent coin tosses, the two random variables X and Y are independent. On the other hand, in other scenarios, it might be more complicated to show whether two random variables are independent.

Example 
I toss a coin twice and define X to be the number of heads I observe. Then, I toss the coin two more times and define Y to be the number of heads that I observe this time. Find P((X<2) and (Y>1))

We can write
P((X<2) and (Y>1))  =P(X<2)P(Y>1)      (because X and Y are independent)
                    =(PX(0)+PX(1))PY(2)
                    =(1/4+1/2)1/4
                    =3/16

We can extend the definition of independence to n random variables.
![alt text](/assets/independentNrv.png)

<iframe width="560" height="315" src="https://www.youtube.com/embed/aeftdFucq-U?si=lEpUEQNhEo_02DSn" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

# Independence of Two Random Variables

Two random variables \(X\) and \(Y\) are independent if the occurrence of one does not affect the probability distribution of the other. Mathematically, \(X\) and \(Y\) are independent if for all \(x\) and \(y\):
$$ P(X = x \text{ and } Y = y) = P(X = x) \cdot P(Y = y) $$

**Example:**
Consider rolling two dice. Let \(X\) be the outcome of the first die and \(Y\) be the outcome of the second die. Since the outcome of one die does not affect the outcome of the other, \(X\) and \(Y\) are independent.

**Real-World Application:**
Independence is crucial in fields like finance, where the independence of stock returns can simplify the modeling of portfolio risks.

!Independence Example
![alt text](/assets/independentCoinToss.png)

Intuitively, two random variables X and Y are independent if knowing the value of one of them does not change the probabilities for the other one. In other words, if X and Y are independent, we can write

P(Y=y|X=x)=P(Y=y), for all x,y

Similar to independent events, it is sometimes easy to argue that two random variables are independent simply because they do not have any physical interactions with each other. Here is a simple example: I toss a coin 2N times. Let X be the number of heads that I observe in the first N coin tosses and let Y be the number of heads that I observe in the second N coin tosses. Since X and Y are the result of independent coin tosses, the two random variables X and Y are independent. On the other hand, in other scenarios, it might be more complicated to show whether two random variables are independent.

Example 
I toss a coin twice and define X to be the number of heads I observe. Then, I toss the coin two more times and define Y to be the number of heads that I observe this time. Find P((X<2) and (Y>1))

Since X
 and Y
 are the result of different independent coin tosses, the two random variables X
 and Y
 are independent. Also, note that both random variables have the distribution we found in Example 3.3. We can write

\[
    P((X<2) and (Y>1))
    =P(X<2)P(Y>1)   (because X and Y are independent)
    =(PX(0)+PX(1))PY(2)
    =(1/4+1/2)1/4
    =3/16 
\]

\[
P(X_1 = 1, X_2 = 3, X_3 = 6) = P(X_1 = 1) \cdot P(X_2 = 3) \cdot P(X_3 = 6) = \frac{1}{6} \times \frac{1}{6} \times \frac{1}{6} = \frac{1}{216}
\]