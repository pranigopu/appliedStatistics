# Hypothesis testing

# 0. Definitions
The following are defined and explained in the file on [approximating distributions](https://github.com/pranigopu/appliedStatistics/blob/60da65c6de1fb42cc2ffb0a1dd8523a3429d937f/expansion/approximatingDistributions.md):

- Population and sample
- Generalising a population's distribution with a random process
- Generalising random sampling as sampling from a random process
- Maintaining the distribution of a random process across samples

_Henceforth, "distribution" = "probability distribution" unless specified._

# 1. Introduction
Let $T$ be a theoretical distribution which models some random process. Now, consider that we want to either (1) study this distribution through its samples or (2) study the samples with respect to $T$ (for example, to try to find out whether these samples are in fact drawn from $T$). Furthermore, case (1) could be a case wherein we want to either (1) try to (1.1) judge the plausibility of an estimate of a parameter of $T$, given that the parameter is unknown, or (1.2) judge the plausbility of a possible $T$ among a family of distributions (considering we know or assume that the random process is distributed by a distribution from this family). In all these cases, we have:

- Theoretical distribution $T$, which may be:
    - Known
    - Assumed
    - Unknown (with only its family known or assumed)
- Samples from a random process (may or may not be modelled by $T$), which may be:
    - Known to be drawn from $T$
    - Assumed to be drawn from $T$
    - Not certain to be drawn from $T$

In the case where everything is known, no further work is needed. But in the case where one or more aspects are assumed or unknown or both, we have a reason to test our assumptions and try to discover a relationship between the samples and the theoretical distribution, if one exists. The use of statistical methods to test assumptions about a theoretical distribution with respect to samples or about samples with respect to a theoretical distribution is hypothesis testing. Alternatively, instead of referring to samples we can refer to "observed random process"; hypothesis testing, then, is the use of statistical methods to test assumptions about the relation between the distribution of an observed random process and a theoretical distribution modelling some random process (which may or may not be the observed random process).

## 1.1. Test statistic
Given a theoretical distribution $T$ (which may be known, assumed or unknown) which is the probability measure $\mathbb{P}$ applied to a given set $X$, a test statistic is an estimator of some parameter of $T$ or a function of an estimator of some parameter of $T$, i.e. it is a collection of maps (collection, because there is a map for each value of $n \in \mathbb{N}$) $T^n:X^n \rightarrow \mathbb{R}$ which implements some operation on any tuple of $X^n$; remember that $X^n = X \times ... \times X$ ($n$ times).
<br><br>

To test how plausible the observed value of the test statistic is, we need to have some idea about the probability distribution of the test statistic itself. The essence of hypothesis testing is figuring out the test statistic's probability distribution (through exact derivations or approximations), then using this distribution to judge the plausibility of an observed value. We ask, in effect, "Given a set of samples as well as the knowledge and assumptions about the samples, the distribution and their relation, is the observed value too extreme?"

## 1.2. Formulating a hypothesis & a test
### 1.2.1. Null hypothesis
To test some aspect of the relation between the observed samples and a theoretical distribution, we form a hypothesis with respect to the relevant test statistic. The simplest way to form a test hypothesis is to form an assumption of no difference, i.e. to hypothesise that there is no difference (i.e. no distance) between the observed random process' distribution and a given theoretical distribution (known or assumed); this is the null hypothesis ("null" refers to "no difference" or "no distance"), notated as $H_0$. We may formulate $H_0$ more precisely, to, for example, make a statement of no difference or distance between:

- An estimate or assumption and the true value of a parameter
- A random process' distribution and a theoretical distribution

In every case, $H_0$ is the hypothesis, either implicitly or explicitly, that the distance between the distribution modelling the observed random process and a given theoretical distribution (known or assumed) is zero. For example, explicitly, $H_0$ may be about the equivalence of an estimate of population mean and the true population mean, but implicitly, $H_0$ holds that the population is distributed by the assumed or estimated distribution whose mean is the given estimated mean.

### 1.2.2. Distribution of the test statistic
A test statistic is an estimator or a function of an estimator of a hypothesised theoretical distribution, hence, its assumed or approximated distribution is derived from the hypothesised one. Hence, tbe able to judge the plausibility of a test statistic's value with respect to a hypothesised theoretical distribution, we have to assume the test statistic's distribution is derived from the hypothesised one. Hence, when we test the plausibility of a test statistic's value, it is always under the assumption that $H_0$ holds, i.e. under the assumption that the null hypothesis is true.

### 1.2.3. Conditions to reject $H_0$
How do we make conclusions, given $H_0$? In essence, we reject $H_0$ if our observation is _deemed_ to be _sufficiently unlikely_. What does this mean?

#### Defining "sufficiently unlikely"
We pick a parameter $\alpha \in (0, 1)$, the **confidence level**. This is a proportion of the most likely (i.e. highest probability) values of the test statistic's distribution. Since the proportion is that of a probability distribution, $\alpha$ is also the probability mass (i.e. combined probability) of the $100 \times \alpha \%$ most likely values of the test statistic. For example, if $\alpha = 0.95$, then it refers to the probability mass of the $95 \%$ most likely values of the test statistic.
<br><br>

The smallest interval containing these values is called the **confidence interval**. Using the confidence interval, we can define what we mean by "sufficiently unlikely"; if an observed value of the test statistic lies outside the confidence interval, i.e. outside the range of the $100 \times \alpha \%$ most likely values of the test statistic, the observed value is deemed "sufficiently unlikely". Usually, $\alpha$ is chosen as $0.95, 0.99, 0.999,$ etc.

#### Critical region
This concept is directly derived from the confidence interval. The critical region is the part of the test statistic's distribution apart from the confidence interval, i.e. the part of the test statistic's distribution containing the $100 \times (1 - \alpha) \%$ least likely values of the test statistic. The probability mass of these values, i.e. $1 - \alpha$, is called the **significance level**. Hence, if an observed value of the test statistic lies within the critical region, it is deemed "sufficiently unlikely".

#### $p$-value
This is an alternative to the critical region to test the plausibility of an observation, and is a concept that is logically and practically equivalent. The $p$-value is the probability mass of all the values of the test statistic that are at least as extreme (i.e. at least as unlikely) as the observed value. If this probability mass is less than the significance level $1 - \alpha$, then we know that the observed value lies in the critical region and is hence deemed "sufficiently unlikely".

#### "One-sided" vs. "two-sided" tests
_Also called "one-tailed" and "two-tailed"_

**NOTE: Meaning of "side of a distribution"**:<br>Given a point $t \in \mathbb{R}$ on the real line:

- "Left side" is the part of the distribution in $(-\infty, t]$
- "Right side" is the part of the distribution in $[t, \infty)$

<br>
Depending on the type of distribution, the critical region, i.e. the $1-\alpha$ proportion of least likely (i.e. most extreme) values may lie on either only one side of the distribution, or on both sides of the distribution.
<br><br>

The parts of the distribution that make up the critical region depend on (1) the shape of the distribution (extent of skewness, concentration of values, etc.) and (2) the confidence level considered. For example, for any symmetric distribution, extreme values lie in equal proportions on both sides, leading to the critical region being equally divided on either side of the distribution. As another example, if the confidence level is low enough, an asymmetric distribution's critical region may lie on both sides of the mean (unequally divided), though for a high enough confidence level, an asymmetric distribution's critical region always lies on only one side of the distribution.
<br><br>

**NOTE: Effect of one or two sidedness on** $p$**-value**: 

Given that $F$ is the cumulative probability distribution of the test statistic and given an observed value $x$, for one-tailed test, $p = \min(1-F(x), F(x))$, whereas for _symmetric_ two-tailed test, $p = 2\min(1-F(x), F(x))$. To understand why, consider what values would be considered "at least as extreme" as the observed value.
