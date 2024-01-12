# Hypothesis testing

# 0. Definitions
The following are defined and explained in the file on [approximating distributions](https://github.com/pranigopu/appliedStatistics/blob/60da65c6de1fb42cc2ffb0a1dd8523a3429d937f/expansion/approximatingDistributions.md):

- Population and sample
- Generalising a population's distribution with a random process
- Generalising random sampling as sampling from a random process

Further definitions unique to this file are given below:

# 1. Introduction
Let $T$ be a theoretical distribution which models a given random process. Now, consider that we want to either (1) study this distribution through its samples or (2) study the samples with respect to $T$ (for example, to try to find out whether these samples are in fact drawn from $T$). Furthermore, case (1) could be a case wherein we want to either (1) try to (1.1) judge the plausibility of an estimate of a parameter of $T$, given that the parameter is unknown, or (1.2) judge the plausbility of a possible $T$ among a family of distributions (considering we know or assume that the random process is distributed by a distribution from this family).
<br><br>
In all the above cases, we have a:

- Theoretical distribution $T$, which may be:
    - Known
    - Assumed
    - Unknown (with only its family known or assumed)
- Samples from a random process, which may be:
    - Known to be drawn from $T$
    - Assumed to be drawn from $T$
    - Not certain to be drawn from $T$

In the case where everything is known, no further work is needed. But in the case where one or more aspects are assumed or unknown or both, we have a reason to test our assumptions and try to discover a relationship between the samples and the theoretical distribution, if one exists. The use of statistical methods to test assumptions about a theoretical distribution or samples with respect to a theoretical distribution is hypothesis testing.

## 1.1. Test statistic
To test how plausible the observed value of the test statistic is, we need to have some idea about the probability distribution of the test statistic as such. The essence of hypothesis testing is figuring out (through exact derivations or approximations) the test statistic's probability distribution, then using this distribution to judge the plausibility of an observed value; We ask, in effect, "Given the data and the assumptions/knowledge about the distribution, is the observed value too extreme?"
