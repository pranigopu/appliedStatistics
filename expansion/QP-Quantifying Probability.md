# Quantifying probability

## 1. Generalising & formalising probability as a measure
_The need for such a generalisation and formalisation is to allow us to talk about probability in an unambiguous but sufficiently generalised context while making the presentation of these ideas more concise (thus easier to retain)_.
<br><br>

What is probability, and when does probability come into the picture? Cognition has two basic states, namely ignorance and knowledge. In ignorance, we have no information about the nature of the object of cognition, so we have no certainty whatsoever about any of its potential. In knowledge, we have all the information about the _essential_ nature of the object of cognition - essential within a given context - to have certainty about its potential, i.e. about how it will act or be acted upon. However, cognition is not binary; when learning of the nature of something, we do not go always from no knowledge to full knowledge - full within a given context. There may be and often are states of cognition for partial information, so that we may know only part of the object's potential. In essence, probability is the quantification of the level of certainty or uncertainty we have regarding some aspect of the potential of some object of cognition, which may be an entity, an environment, a phenomenon, etc. 

### Random process (_a preliminary concept_)
Random process is a process with a defined set of possible outcomes wherein one or all factors key to its outcomes are unknown, for practical or other reasons. A process is specific aspect of the behaviour of an object of cognition, while an outcome is specific aspect of the potential of this object regarding this behaviour. Thus, "random process" generalises the concept of a specific aspect of the behaviour an unknown object of cognition in a specific context which we can only come to know - for practical or other reasons - by observing the outcomes it produces. Hence, we can generalise the concept of probability as the quantification of the information we have about potential outcomes of a random process.

### Quantifying probabilities as proportions
Let us begin by quantifying certainty about a certain outcome as $1$ and $0$, wherein $1$ quantifies the certainty of the outcome being observed and $0$ quantifies the certainty of the outcome not being observed. We do not choose these values arbitrarily; they are based on the idea of expected proportions. If something is certain to be observed in a given context, we expect it to be observed in $100$% of the cases wherein the given context holds. Similarly, if something is certain to not be observed in a given context, we expect it to be observed in $0$% of the cases wherein the context holds. If we are uncertain, our expectation has to be between $0$% and $100$%, since an uncertain outcome may be observed only some of the times, i.e. some proportion of the times less than $1$ but greater than $0$. In this light, we see that probability is the quantification of expectations (more specifically, the expectations about the outcomes of a random process).

### Measure
Consider a random process $\theta$. It is clear that some but any outcome of $\theta$ will certainly be observed; we have this certainty at any moment. At a given moment, since each set of outcomes of $\theta$ have some probability of being observed but the probability of observing some but any outcome of $\theta$ is $1$, it follows that sum of the probabilities of each pairwise disjoint subset of outcomes that together make up the set of all possible outcomes is $1$. In other words, each of these subsets of outcomes may be expected to be observed in only some proportion of cases, but together, their proportion of being observed must add up to $1$ as together they make up the whole of the potential of $\theta$ in the given context. Seeing probabilities as "proportional" potential helps us see that the probability of any subset of the set of all possible outcomes is a part of the whole. It is handy, then, that there is a concept that formalises such "proportional" quantification of a set, namely, the concept of "measure". Using this concept, we can define probability as a kind of measure, thus being able to apply the properties of measures in general to probabilities in particular.
<br><br>

A measure is a function that maps each subset of a given set $X$ to a non-negative real value called "mass" (_the non-negativity property_), such that the mass of $X$ as a whole is the total mass of pairwise disjoint subsets of $X$ that together make up $X$ (_the additivity property_). Note, of course, that the subset may be a set with but one element. A measure generalises and formalises the concept of quantifying some aspect of each subset of a set that is present in the subset as a part of the whole. For example, a counting measure quantifies the size of a subset; each subset's size is a part of the size of the set as a whole. Other examples of measures present in subsets of a set as parts of a whole are area of a shape and its parts, volume of a solid and its parts, the probability of some and all of the outcomes of a random process, etc.

### Probability measure & distribution
A probability measure is the formalisation of probability as a kind of measure. Often denoted as $\mathbb{P}$, a probability measure is a measure that maps each subset of a given set to a real value from $0$ to $1$ called "probability mass", with the probability mass of the set as a whole being $1$. Given that it formalises the concept of the probability of outcomes of a given random process, it is clear that the way mapping between outcomes and probabilities is done depends on the random process in question. This reinforces the fact that "probability measure" as such is a kind of measure, i.e. as such, it refers to a class of measures; a probability measure $\mathbb{P}$ applied to a particular random process represents a particular _distribution_ of probabilities. To rephrase, **_a probability distribution is a probability measure applied to a particular random process_**.

## 2. Studying populations with probability
Now, we shall define (if necessary) and integrate the concepts of population, random process, sample and random sample. We do this to integrate the idea of probability to the wider concept of studying non-enumerable classes of entities or events using data. Why is this necessary?
<br><br>

A non-enumerable class is one whose members cannot all be studied, making the class "unlimited", either only in practice or in both theory and practice. To study the nature of the members of a non-enumerable class as a whole (i.e. in general), we need to make generalisations, through either induction or statistics (i.e. measurements on raw data); the statistical approach is weaker, but in many cases, it is the only approach that can be taken. When we need to study a non-enumerable class using the data of samples drawn from it, we deal with uncertainty about the characteristics of the class as a whole. This is because samples are particulars; using data alone without induction, universals can only be approximated from particulars (_universals also cannot be deduced from particulars_). Hence, drawing and measuring samples from the population is part of a random process, which makes probability measures the right tools to study such a class further in such a context.

### Population
The set of all elements in a class of similar elements, i.e. the set of all units of a specific kind. This can be the set of all...

- ... possible outputs of a random process
- ... possible outcomes of a random experiment
- ... entities of a specific kind

##### Generalising population distribution with random process
A random process can be used to generalise the distribution of some metric of a population's individuals as the probability distribution of that metric for a random selection of individuals from the population; here, the random selection is the random process. Thus, a distribution of the population, which may be defined in terms of frequency, density or probability, can be generalised as the probability distribution that serves as the theoretical model for a random process. Hence, when referring the a population distribution, we shall always use the term "theoretical distribution".

**NOTE**: _We generalise the population distribution, not the population itself!_

#### Sample
A single individual drawn from a population. There are many sampling methods, such as random sampling, selective sampling, systematic sampling, etc. However, we shall see how and why we use random sampling with replacement.

#### Random sample
A single sample, i.e. a single outcome drawn from a random process.
<br><br>

**NOTE 1: "Sampling from a distribution"**:<br>If we know or assume the random process follows a specific probability distribution, or alternatively, if we define a random or pseudorandom process that is designed to follow a specific probability distribution, then the sample is said to be drawn from the given distribution.

**NOTE 2: Random sample from a population**:<br>Drawing a random sample from a population is the same as drawing a sample from a random process, wherein the random process here is the random selection from the population. This is another way of expressing random sampling, but this is done to make the phrase "sample from a random process" both generalised and unambiguous. This is done to make the expression of related ideas clear and concise.

## TERMINOLOGY CHECKPOINT
Clarifying the meaning of some phrases used later that use terms defined so far...

|Term/phrase|Meaning|
|--- |--- |
|Sample space of random process $\theta$|The set of all possible outcomes of $\theta$|
|Drawing from a distribution|Drawing a sample from the random process modelled by the given distribution|
|Distribution defined for random process $\theta$|Distribution which models $\theta$|
|Distribution defined on a set $X$|Distribution defined for some random process whose sample space is $X$|

## 3. Mathematically defining probability distributions
In the previous section, we defined probability distributions as measures, specifically as probability measures. Thus, mathematics being the science of measurement is the science we must use to explore probability distributions. To do this, we must express probability distributions as mathematical objects.

### Cumulative distribution function
Formally, a cumulative distribution function (CDF) of a probability distribution $\mathbb{P}$ defined on a set $X$ is given by:

$CDF(t) = \mathbb{P}((-\infty, t])$

i.e. the CDF value of any point $t$ is the cumulative probability mass upto $t$, i.e. the probability mass of all values less than or equal to $t$.