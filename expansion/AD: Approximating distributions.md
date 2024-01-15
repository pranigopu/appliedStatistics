# Approximating distributions

## CONTENTS
- [0. Definitions](#0-definitions)
  - [0.1. Population, random process, sample \& sample space](#01-population-random-process-sample--sample-space)
    - [0.1.1. Population](#011-population)
    - [0.1.2. Random process](#012-random-process)
      - [0.1.2.1. Generalising population distribution with random process](#0121-generalising-population-distribution-with-random-process)
      - [0.1.2.2. Maintaing probability distribution across samples](#0122-maintaing-probability-distribution-across-samples)
    - [0.1.3. Sample](#013-sample)
    - [0.1.4. Random sample](#014-random-sample)
    - [0.1.5. Sample space](#015-sample-space)
  - [0.2. Product measure](#02-product-measure)
    - [0.2.1. Product measure of a probability measure](#021-product-measure-of-a-probability-measure)
  - [0.3. Definitions related to distributions](#03-definitions-related-to-distributions)
    - [0.3.1. Support of a distribution](#031-support-of-a-distribution)
    - [0.3.2. Spread of a distribution](#032-spread-of-a-distribution)
    - [0.3.3. Sum of two distributions](#033-sum-of-two-distributions)
    - [0.3.4. Distribution parameter functions](#034-distribution-parameter-functions)
    - [0.3.5. "Drawing from a distribution"](#035-drawing-from-a-distribution)
- [1. Estimators](#1-estimators)
  - [1.1. Distribution of an estimator](#11-distribution-of-an-estimator)
  - [1.2. Properties of estimators](#12-properties-of-estimators)
  - [1.3. Some noteworthy estimators](#13-some-noteworthy-estimators)
- [2. Limit laws](#2-limit-laws)
  - [2.1. Laws of large numbers](#21-laws-of-large-numbers)
    - [2.1.1. Weak law of large numbers](#211-weak-law-of-large-numbers)
    - [2.1.2. Strong law of large numbers](#212-strong-law-of-large-numbers)
  - [2.2. Central limit theorem](#22-central-limit-theorem)

## 0. Definitions

### 0.1. Population, random process, sample & sample space
#### 0.1.1. Population
The set of all elements in a class of similar elements, i.e. the set of all units of a specific kind. This can be the set of all...

- ... possible outputs of a random process
- ... possible outcomes of a random experiment
- ... entities of a specific kind

#### 0.1.2. Random process
A process with one or more factors that - for practical or other reasons - cannot be accounted for.

##### 0.1.2.1. Generalising population distribution with random process
A random process can be used to generalise the distribution of some metric of a population's individuals as the probability distribution of that metric for a random selection of individuals from the population; here, the random selection is the random process. Thus, a distribution of the population, which may be defined in terms of frequency, density or probability, can be generalised as the probability distribution that serves as the theoretical model for a random process. Hence, when referring the a population distribution, we shall always use the term "theoretical distribution".

**NOTE**: _We generalise the population distribution, not the population itself!_

##### 0.1.2.2. Maintaing probability distribution across samples
_Henceforth, "distribution" = "probability distribution" unless specified._
<br><br>

_Maintaining the distribution of a random process across samples_...<br>The probability distribution of a random process is maintained across samples, i.e. for each sample only if each outcome of the process is independent of past outcomes. Maintaining the probability distribution for each sample is needed when studying this distribution through its samples.

_Maintaining the distribution of a random selection across selections_...<br>_Note that a random selection is a kind of random process_. Any sequence of random selections from a population are independent if they are made with replacement (_more on sampling with replacement later_), i.e. if at each selection, each set of metric values have a probability of being observed that stays the same regardless of whether they were observed before. Note that practically, for a large enough population with respect to the number of samples taken, the distribution from random sampling without replacement can still be generalised as a distribution from a random process whose distribution is maintained across samples, given the negligible (near-zero) change in the distribution of the metric being studied among the population's individuals even as samples are drawn without replacement.

#### 0.1.3. Sample
A single individual drawn from a population. There are many sampling methods, such as random sampling, selective sampling, systematic sampling, etc. However, we shall see how and why we use random sampling with replacement.

#### 0.1.4. Random sample
A single sample, i.e. a single outcome drawn from a random process.
<br><br>
**NOTE 1: "Sampling from a distribution"**:<br>If we know or assume the random process follows a specific probability distribution, or alternatively, if we define a random or pseudorandom process that is designed to follow a specific probability distribution, then the sample is said to be drawn from the given distribution.

**NOTE 2: Random sample from a population**:<br>Drawing a random sample from a population is the same as drawing a sample from a random process, wherein the random process here is the random selection from the population. This is another way of expressing random sampling, but this is done to make the phrase "sample from a random process" both generalised and unambiguous. This is done to make the expression of related ideas clear and concise.

#### 0.1.5. Sample space
The sample space of a random process is the set of all possible outcomes of the random process.

### 0.2. Product measure
$M_1 \bigotimes M_2$ denotes the product measure of $M_1$ and $M_2$, given that $M_1$ and $M_2$ are measures defined on sets $X$ and $Y$ respectively. $M_1 \bigotimes M_2$ is the product measure defined on $X \times Y$ such that:

$(M_1 \bigotimes M_2)(A \subseteq X \times Y) = M_1(A)M_2(A)$

**NOTE**: We denote:

- $X \times ... \times X$ ($n$ times) as $X^n$
- $M \bigotimes ... \bigotimes M$ ($n$ times) as $M^n$

#### 0.2.1. Product measure of a probability measure
A product measure of a probability measure is the product measure of two or more copies of the probability measure, and results in an independent joint probability distribution (_independent means that no component of the joint outcome affects the others_); this represents the joint distribution of tuples of $n$ independently drawn samples.

### 0.3. Definitions related to distributions
#### 0.3.1. Support of a distribution
The set of values for which the mass (for discrete distributions) or density (for continuous distributions) is non-zero. Furthermore, we can define the support of a probability distribution as the smallest set of values for which the probability mass is $1$.

#### 0.3.2. Spread of a distribution
The deviation of distributed values from the distribution mean. This can be measured in many ways, such as variance, standard deviation, mean deviation, interquartile range, etc. In a probability distribution, convergence of the spread of the distribution to a specific interval refers to the asymptotic rise with respect to some variable $k$ in the proportion of the mass of the distribution concentrated in the interval. Asymptotic rise in proportion means that the proportion capable of reaching arbitrarily close to $1$, given a large enough $k$.

#### 0.3.3. Sum of two distributions
Given:

- $\displaystyle +:\mathbb{R} \rightarrow \mathbb{R}, (x_1, x_2 ... x_n) \mapsto \sum_{i=1}^n x_i$
- $\mathbb{P}$ defined on a set $X \subseteq \mathbb{R}$

We define:

$\mathbb{P} + ... + \mathbb{P}$ ($n$ times) $= +_*(\mathbb{P}^n)$

**NOTE**: We denote:

- $\mathbb{P} + ... + \mathbb{P}$ ($n$ times) as $\mathbb{P}_n$
- $\frac{1}{n}\mathbb{P}_n$ as $\bar{\mathbb{P}}_n$

#### 0.3.4. Distribution parameter functions
$\mu$<br>
Distribution mean function, i.e. a function that inputs a probability measure defined on a given set $S$ and outputs the corresponding distribution's mean (if it exists).

$Var$<br>
Distribution variance function, i.e. a function that inputs a probability measure defined on a given set $S$ and outouts the corresponding distribution's variance (if it exists).

#### 0.3.5. "Drawing from a distribution"
This is shorthand for "drawing from the random process modelled by the given distribution".

## 1. Estimators
_Henceforth, "distribution" = "probability distribution" unless specified._
<br><br>

An estimator is a collection of maps (collection, because there is a map for each value of $n \in \mathbb{N}$) $T^n:X^n \rightarrow \mathbb{R}$ which implements some operation on any tuple of $X^n$. The purpose of an estimator is to estimate some real value related to the probability measure on $X$, such as the distribution mean, variance, etc.
<br><br>

**NOTE: Independent and identically distributed (IID) samples as a prerequisite for estimation**:<br>The essence of estimation is averaging; we average over many samples from a distribution to get an idea about the distribution itself. To do this, we must first ensure a lack of dependence between consequent samples, since such dependence changes the distribution of consequent samples. In the same vein, since estimation depends on averaging samples from the same distribution, we need to ensure the samples are drawn from the same distribution, i.e. we need to ensure the samples are identically distributed.

### 1.1. Distribution of an estimator
Consider a theoretical distribution $\mathbb{P}$ which models a given random process whose sample space is $X$. Given an estimator $T^n:X^n \rightarrow \mathbb{R}$ (for all $n$) which estimates some parameter of $\mathbb{P}$, the distribution the estimator is essentially the pushforward measure of $\mathbb{P}^n$ through $T^n$, i.e. $T^n_*\mathbb{P}^n$. This can be understood as the distribution of the results of applying a function $T^n$ to $n$ samples each drawn from $\mathbb{P}$.

### 1.2. Properties of estimators
These properties support the purpose of estimators; an estimator without one or both of these properties cannot be used for an accurate estimation of distribution parameters. Now, given we have an estimator $T^n$ meant to estimate the parameter $\phi(\mathbb{P})$ of the distribution $\mathbb{P}$...

1. **Unbiasedness**<br>$\mu({T^n}_*\mathbb{P}^n) = \phi(\mathbb{P})$
2. **Consistency**<br>$\displaystyle \lim_{n \rightarrow \infty} T^n_*\mathbb{P}^n([\phi(\mathbb{P}) - \epsilon, \phi(\mathbb{P}) + \epsilon]) = 1, \forall \epsilon > 0$

In words, unbiasedness implies that the mean of the distribution of the estimator values equals to the parameter to be estimated. Consistency implies that as the number of samples taken rises, the mass of the distribution of estimator values converges to an arbitrarily small neighbourhood around the parameter to be estimated.

### 1.3. Some noteworthy estimators

1. Sample mean, distributed by $\bar{\mathbb{P}}_n$
2. Sample variance, distributed by $\frac{1}{n}(\mathbb{(P-\mu(\mathbb{P})}^n)$

**MORE ON SAMPLE MEAN DISTRIBUTION**:<br>
The sample mean distribution is such that....

- $\mu(\bar{\mathbb{P}}_n) = \mu({\mathbb{P}}) \implies$ unbiasedness
- $Var(\bar{\mathbb{P}}_n) = \frac{Var(\mathbb{P})}{n} \implies$ consistency

## 2. Limit laws
Limit laws are results about the convergence of the sample mean distribution as the number of samples taken increases. Why does this matter? The distribution over which we take sample means may be any distribution, including the distribution of an estimator values. Since the essence of estimation is averaging, it helps to know how averages behave as the number of samples taken increases. Note that, as with estimators, all limit laws presuppose that (1) samples are drawn independently and (2) samples are drawn from the same distribution. In other words, we only deal with independently and identically distributed (IID) samples.

### 2.1. Laws of large numbers
These laws are results about the convergence of spread of the sample mean distribution.

#### 2.1.1. Weak law of large numbers
$\displaystyle \lim_{n \rightarrow \infty} \bar{\mathbb{P}}_n([\mu(\mathbb{P}) - \epsilon, \mu(\mathbb{P}) + \epsilon]) = 1, \forall \epsilon > 0$

In words, as the number of samples taken $n$ taken from a given distribution increases, the spread of the sample mean distributions converges to an arbitrarily small interval around the given distribution's mean. In other words, averaging over larger numbers of samples leads to more precise estimates.

#### 2.1.2. Strong law of large numbers
$\displaystyle \mathbb{P}^{\infty}(\{(x_1, x_2 ...) | \lim_{n \rightarrow \infty}\frac{1}{n}\sum_{i=1}^n x_i = \mu(\mathbb{P})\}) = 1$

**NOTE**: $\mathbb{P}^{\infty} = \mathbb{P} \bigotimes \mathbb{P} \bigotimes ...$

In words, given infinite (i.e. _potentially_ limitless) IID samples from a given distribution, it is certain that sample means of any number of these samples taken converges to the given distribution's mean as the number of these samples taken rises. Another way to word the law is to say that the spread of the joint distribution of infinite (i.e. _potentially_ limitless) IID samples from a given distribution is exactly the set of all values whose subsets' sample means converge to the given distribution's mean as the subsets' size rises. This implies that sample mean of any sequence of IID samples will converge to the given distribution's mean as more IID samples are added to the sequence.

### 2.2. Central limit theorem
This is a result about the convergence of the sample mean distribution as a whole to a normal distribution, as the number of samples taken rises. In essence, this result helps approximate the sample mean distribution as a normal distribution, especially when the number of samples taken is very large.

$\displaystyle \lim_{n \rightarrow \infty} \sqrt{n}(\bar{\mathbb{P}}_n - \mu(\mathbb{P}))((-\infty, t]) = \text{Normal}(0, \sqrt{Var(\mathbb{P})})((-\infty, t])$

---

We can reformulate the above in less precise terms as:

- $\sqrt{n}(\bar{\mathbb{P}}_n - \mu(\mathbb{P})) \approx \text{Normal}(0, \sqrt{Var(\mathbb{P})})$ as $n \rightarrow \infty$
- $\frac{\sqrt{n}(\bar{\mathbb{P}}_n - \mu(\mathbb{P}))}{Var(\mathbb{P})} \approx \text{Normal}(0, 1)$ as $n \rightarrow \infty$
- $\bar{\mathbb{P}}_n \approx \text{Normal}(\mu(\mathbb{P}), \sqrt{\frac{Var(\mathbb{P})}{n}})$ as $n \rightarrow \infty$

**NOTE**: " $\approx$ " _here means "approximately the same as"._

The purpose of the above reformulations is to help understand what the central limit theorem means and how it could be used in approximating a sample mean distribution. The last three formulations may be less precise, but they show that it is the sample mean distribution that is being estimated, and that can be approximated directly if needed.
