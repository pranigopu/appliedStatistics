# Estimators & hypothesis testing

## Definitions

### Sample
A sample is a single outcome drawn from a random process. If we know or assume the random process follows a certain probability distribution, or alternatively, if we define a random or pseudorandom process that is designed to follow a certain probability distribution, then the sample is said to be drawn from the given distribution.

### Probability measure
$\mathbb{P}$ denotes the probability measure, i.e. a measure defined on a given set $S$ that inputs a subset of $S$ and outputs that subset's probability mass such (a value between $0$ and $1$) such that the probability mass of $S$ is $1$.

### Product measure
$M_1 \bigotimes M_2$ denotes the product measure of $M_1$ and $M_2$, given that $M_1$ and $M_2$ are measures defined on sets $X$ and $Y$ respectively. $M_1 \bigotimes M_2$ is the product measure defined on $X \times Y$ such that:

$(M_1 \bigotimes M_2)(A \subseteq X \times Y) = M_1(A)M_2(A)$

**NOTE**: We denote:

- $X \times ... \times X$ ($n$ times) as $X^n$
- $M \bigotimes ... \bigotimes M$ ($n$ times) as $M^n$

#### Product measure of a probability measure
A product measure of a probability measure is the product measure of two or more copies of the probability measure, and results in an independent joint probability distribution (_independent means that no component of the joint outcome affects the others_). Hence, $\mathbb{P}^n$ represents the distribution of tuples of $n$ independently drawn samples.

### Sum of two distributions
Given:

- $+:\mathbb{R} \rightarrow \mathbb{R}, (x_1, x_2 ... x_n) \mapsto \sum_{i=1}^n x_i$
- $\mathbb{P}$ defined on a set $X \subseteq \mathbb{R}$

$\mathbb{P} + ... + \mathbb{P}$ ($n$ times) $= +_*(\mathbb{P}^n)$

**NOTE**: We denote:

- $\mathbb{P} + ... + \mathbb{P}$ ($n$ times) as $\mathbb{P}_n$
- $\frac{1}{n}\mathbb{P}_n$ as $\bar{\mathbb{P}_n}$

### Distribution parameter functions
$\mu$<br>
Distribution mean function, i.e. a function that inputs a probability measure defined on a given set $S$ and outputs the corresponding probability distribution's mean (if it exists).

$Var$<br>
Distribution variance function, i.e. a function that inputs a probability measure defined on a given set $S$ and outouts the corresponding probability distribution's variance (if it exists).

## Estimators
**NOTE**: _Henceforth, "distribution" = "probability distribution" unless specified._
<br><br>
An estimator is a collection of maps (_collection, because there is a map for each value of $n \in \mathbb{N}$) $T^n:X^n \rightarrow \mathbb{R}$ which implements some operation on any tuple of $X^n$. The purpose of an estimator is to estimate some real value related to the probability measure on $X$, such as the distribution mean, variance, etc.
<br><br>
The essence of such estimation is averaging; we average over many samples from a distribution to get an idea about the distribution itself. To do this, we must first ensure a lack of dependence between consequent samples, since such dependence changes the distribution of consequent samples.

### Properties of estimators
These properties support the purpose of estimators; an estimator without one or both of these properties cannot be used for an accurate estimation of distribution parameters. Now, given we have an estimator $T^n$ meant to estimate the parameter $\phi(\mathbb{P})$ of the distribution corresponding to $\mathbb{P}$...

1. **Unbiasedness**<br>$\mu({T^n}_*\mathbb{P}^n) = \phi(\mathbb{P})$
2. **Consistency**<br>$\displaystyle \lim_{n \rightarrow \infty} {T^n}_*\mathbb{P}^n([\phi(\mathbb{P}) - \epsilon, \phi(\mathbb{P}) + \epsilon]) = 1$, $\forall \epsilon > 0$

In words, unbiasedness implies that the mean of the distribution of the estimator values equals to the parameter to be estimated. Consistency implies that as the number of samples rises, the distribution of estimator values converges to a small neighbourhood around the parameter to be estimated.

### Some noteworthy estimators

1. Sample mean, distributed by $\bar{\mathbb{P}_n}$
2. Sample variance, distributed by $\frac{1}{n}(\mathbb{(P-\mu(\mathbb{P})}^n)$

**MORE ON SAMPLE MEAN DISTRIBUTION**:<br>
The sample mean distribution is such that....

- $\mu(\bar{\mathbb{P}_n}) = \mu({\mathbb{P}}) \implies$ unbiasedness
- $Var(\bar{\mathbb{P}_n}) = \frac{Var(\mathbb{P})}{n} \implies$ consistency
