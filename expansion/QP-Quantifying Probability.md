# Quantifying probability

## 1. Generalising & formalising probability as a measure
_The need for such a generalisation and formalisation is to allow us to talk about probability in an unambiguous but sufficiently generalised context while making the presentation of these ideas more concise (thus easier to retain)_.
<br><br>

What is probability, and when does probability come into the picture? Cognition has two basic states, namely ignorance and knowledge. In ignorance, we have no information about the nature of the object of cognition, so we have no certainty whatsoever about any of its potential. In knowledge, we have all the information about the _essential_ nature of the object of cognition - essential within a given context - to have certainty about its potential, i.e. about how it will act or be acted upon. However, cognition is not binary; when learning the nature of something, we do not go always from no knowledge to full knowledge - full within a given context. There may be and often are states of cognition for partial information, so that we may know only part of the object's potential. In essence, probability is the quantification of the level of certainty or uncertainty we have regarding some aspect of the potential of an object of cognition, which may be an entity, an environment, a phenomenon, etc. 

### Random process (_a preliminary concept_)
Random process is a process with a defined set of possible outcomes wherein one or all factors key to its outcomes are unknown, for practical or other reasons. A process is specific aspect of the behaviour of an object of cognition, while an outcome is specific aspect of the potential of this object regarding this behaviour. Thus, "random process" generalises the concept of a specific aspect of the behaviour an unknown object of cognition in a specific context which we can only come to know - for practical or other reasons - by observing the outcomes it produces. Hence, we can generalise the concept of probability as the quantification of the information we have about potential outcomes of a random process.

### Quantifying probabilities as proportions
Let us begin by quantifying certainty about a certain outcome as $1$ and $0$, wherein $1$ quantifies the certainty of the outcome being observed and $0$ quantifies the certainty of the outcome not being observed. We do not choose these values arbitrarily; they are based on the idea of expected proportions. If something is certain to be observed in a given context, we expect it to be observed in $100$% of the cases wherein the given context holds. Similarly, if something is certain to not be observed in a given context, we expect it to be observed in $0$% of the cases wherein the context holds. If we are uncertain, our expectation has to be between $0$% and $100$%, since an uncertain outcome may be observed only some of the times, i.e. some proportion of the times less than $1$ but greater than $0$. In this light, we see that probability is the quantification of expectations (more specifically, the expectations about the outcomes of a random process).
<br><br>

The idea of probability as the proportion of times we expect to observe an outcome does not make sense for rare or once-in-a-lifetime outcomes or random processes that produce such outcomes. However, the idea of probability as proportion makes sense if you consider not the number of times we expect to observe an outcome in reality, but rather, the number of possible _hypothetical_ states in which we expect the outcome to be observed. A possible or hypothetical state here refers to a state of the environment in question that can be hypothesised based on what we know; of course, a hypothesis implies assumptions about unknowns, i.e. it refers to a possibility given our knowledge, which may or may not be true now or ever.

### Measure
Consider a random process $\theta$. It is clear that some but any outcome of $\theta$ will certainly be observed; we have this certainty at any moment. At a given moment, since each set of outcomes of $\theta$ have some probability of being observed but the probability of observing some but any outcome of $\theta$ is $1$, it follows that sum of the probabilities of each pairwise disjoint subset of outcomes that together make up the set of all possible outcomes is $1$. In other words, each of these subsets of outcomes may be expected to be observed in only some proportion of cases, but together, their proportion of being observed must add up to $1$ as together they make up the whole of the potential of $\theta$ in the given context. Seeing probabilities as "proportional" potential helps us see that the probability of any subset of the set of all possible outcomes is a part of the whole. It is handy, then, that there is a concept that formalises such "proportional" quantification of a set, namely, the concept of "measure". Using this concept, we can define probability as a kind of measure, thus being able to apply the properties of measures in general to probabilities in particular.
<br><br>

A measure is a function that maps each subset of a given set $X$ to a non-negative real value called "mass" (_the non-negativity property_), such that the mass of $X$ as a whole is the total mass of pairwise disjoint subsets of $X$ that together make up $X$ (_the additivity property_). Note, of course, that the subset may be a set with but one element. A measure generalises and formalises the concept of quantifying some aspect of each subset of a set that is present in the subset as a part of the whole. For example, a counting measure quantifies the size of a subset; each subset's size is a part of the size of the set as a whole. Other examples of measures present in subsets of a set as parts of a whole are area of a shape and its parts, volume of a solid and its parts, the probability of some and all of the outcomes of a random process, etc.

### Probability measure & distribution
A probability measure is the formalisation of probability as a kind of measure. Often denoted as $\mathbb{P}$, a probability measure is a measure that maps each subset of a given set to a real value from $0$ to $1$ called "probability mass", with the probability mass of the set as a whole being $1$. Given that it formalises the concept of the probability of outcomes of a given random process, it is clear that the way mapping between outcomes and probabilities is done depends on the random process in question. This reinforces the fact that "probability measure" as such is a kind of measure, i.e. as such, it refers to a class of measures; a probability measure $\mathbb{P}$ applied to a particular random process represents a particular _distribution_ of probabilities. To rephrase, **_a probability distribution is a probability measure applied to a particular random process_**.

## 2. Studying populations with probability
Now, we shall define (if necessary) and integrate the concepts of population, random process, sample and random sample. We do this to integrate the idea of probability to the wider concept of studying non-enumerable classes of entities or events using data, thus integrating probability to the study of statistics in a wider sense. Why is this relevant?
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
A single individual drawn from a population.
<br><br>

**NOTE**: There are many sampling methods (random sampling, selective sampling, systematic sampling, etc.). However, random sampling with replacement is the one we shall use and the reason will become clear in the following subsections.

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
|Sample space of distribution $\mathbb{P}$|The set of all possible outcomes of the random process modelled by $\mathbb{P}$|
|Drawing from a distribution|Drawing a sample from the random process modelled by the given distribution|
|Distribution defined for random process $\theta$|Distribution which models $\theta$|
|Distribution defined on a set $X$|Distribution defined for some random process whose sample space is $X$|

## 3. Probability distributions for transformed spaces
Here, we shall see a way in which formalising probability as a kind of measure is useful in expanding the use of probability distributions. In particular, if we have a random process whose outcomes are transformed by a function, we can obtain the distribution of these transformed outcomes using the distribution of the untransformed outcomes. 
<br><br>

_First, a key concept_...

### Pushforward measure
Let measure $M$ be defined for a set $X$ in a specific context. Now, consider a set $Y$ wherein, in this context, each element of $Y$ is a function of an element in $X$, i.e. there is a function $f$ such that $f(x) = y, \forall (x, y) \in X \times Y$. Hence, note that $f$ is surjective, i.e. every image (output of the function) has a preimage (input to the function). Then, the pushforward measure of $M$ through $f$ is given by:

$f_*M(y) = M(f^{-1}(y)) = M(\{x | f(x) = y, x \in X\})$

**NOTE**: $f^{-1}$ is the inverse function of $f$, defined such that it inputs an element $y$ of $Y$ and outputs the element or elements of $X$ that map to $y$ through $f$.

### Pushforward probability measure
Let $\mathbb{P}$ be a probability distribution defined for a random process $\theta$ whose sample space is $X$. Now, consider the sample space $Y$ of $\theta$ after transforming any and every outcome of $\theta$ by a function $f$. It is clear that since the transformed outcomes come from the same core random process, their distribution can be derived from the distribution of the untransformed outcomes, namely $\mathbb{P}$. In particular, we can see that the probability mass of any subset of values $B$ in $Y$ is exactly the probability mass of the set of all values in $X$ that map to the values in $B$, because (1) the values in $B$ are but a subset of transformed outcomes of $\theta$ and (2) the sample space of $\theta$ is $X$. Hence, the probability mass of $B$ is given by:

$\mathbb{P}(\{x | f(x) = y \in B, x \in X\}) = \mathbb{P}(f^{-1}(B))$

But this is exactly the pushforward measure of $\mathbb{P}$ through $f$ applied to $B$, i.e. $f_*\mathbb{P}(B)$. Hence, we see the use of pushforward in formalising the idea of applying a distribution of outcomes to a transformation of these outcomes using the transformation function.

## 4. Mathematically defining probability distributions
In the previous section, we defined probability distributions as measures, specifically as probability measures. Thus, mathematics being the science of measurement is the science we must use to explore probability distributions. To do this, we must express probability distributions as mathematical objects.

### Cumulative distribution function
 Consider a probability distribution $\mathbb{P}$ defined for a random process $\theta$ whose sample space is $X$. Then, formally, the cumulative distribution function (CDF) $F$ of $\mathbb{P}$ at the point $x \in X$ is given by:

$F(x) = \mathbb{P}((-\infty, t])$

i.e. the CDF value of any point $x$ is the cumulative probability mass upto $x$, i.e. the probability mass of all values less than or equal to $x$. $-\infty$ here only represents the idea of not fixing a lower bound; we want to include any and every point that may be below $x$, regardless of the given distribution's sample space. In practice, there may be a lower bound $b$ below which the probability mass is always zero; in such a case, the interval $(-\infty, x]$ can be replaced by $[b, x]$.

Why define the CDF? The CDF allows us to _conveniently_ study the proportional effect of a change in the probability mass at a specific point in the sample space (proportional $\implies$ with respect to the total probability mass $1$) as well as the rate of the change at that point. Of course, we can simply use the probability measure as seen above, but the concept CDF offers economy in thought, reference and notation.

### Probability density function
_First, some buildup_...
<br><br>

Let $\mathbb{P}$ be a probability distribution defined for a random process $\theta$ whose sample space is $X$. Let $F$ be the CDF of $\mathbb{P}$. Now, given a point $x \in X$, consider the following:

- $F(x) = \mathbb{P}((-\infty, x])$ (_definition of CDF_)
- $\mathbb{P}([a, b]) = \mathbb{P}((-\infty, b]) - \mathbb{P}((-\infty, a]) = F(b) - F(a)$

---

_Now, set aside the above for a moment and consider the first-order derivative of_ $F$, _i.e._ $F^1$...

Integrating $F^1$ for the interval $[a, b]$ results in:

$\displaystyle \int_a^b F^1(t) dt = [F(t)]_b^a = F(b) - F(a)$

---

With this result, we have that:

$\displaystyle \mathbb{P}([a, b]) = \int_a^b F^1(t) dt$

_Now, to define the topic at hand_...
<br><br>

Hence, we get $F^1$ as the function such that its integral for any interval $[a, b]$ is the probability mass of that interval under the distribution $\mathbb{P}$. In other words, $F^1$ is a curve such that the area under the curve for any interval represents the probability mass of that interval under the distribution $\mathbb{P}$. From this, we can see that $F^1$ is valuable to help visualise, conceptualise and thus study the spread of the mass of the distribution.
<br><br>

Now, also consider what $F^1(x)$ represents for any point $x$ in the sample space. Evidently, it is the gradient, i.e. rate of change of the cumulative probability mass at that point. A higher gradient represents a higher rise in probability mass at that point, which shows a higher concentration of the probability mass in a small neighbourhood of that point. Thus, we term the gradient of the cumulative probability mass at a point as the probability density at the point.
<br><br>

To reinforce the last few statements...

1. Comparing the probability densities of each of two points in the sample space indicates a small neighbourhood of the point where there is a higher proportion of the total probability mass compared to the same small interval of the other point.
2. Comparing the way the probability density values for each of two distributions helps us compare the way outcomes from each distribution are expected to be spread over space, time, the population or some other metric.
3. The key purpose of probability density is to study the spread of the distribution, i.e. to study how and in what proportions is the total probability mass concentrated across the sample space.

<br>

Probability density is hence a useful concept, albeit a more abstract concept than probability mass. Of course, just as with CDF, we can study the spread of the distribution using the probability measure and the derivatives of cumulative probability mass, but the concept a probability density function, i.e. PDF offers economy in thought, reference and notation. For convenience, we shall notate the PDF $F^1$ as $f$. Just to clarify, given a point $x$ in the sample space:

- $f(x) = \frac{d \mathbb{P}((-\infty, x])}{dx} = \frac{d F(x)}{dx} = F^1(x)$
- **_Probability density defined at a point_** $x$ **_is the gradient of the cumulative probability mass at_** $x$

<br>

**NOTE: The domain of CDF and PDF**:<br>Both the CDF and the PDF are defined not for intervals but single points in the sample space; they are less generalised functions than a probability measure and have to be treated as specific kinds of operations using the probability measure.
