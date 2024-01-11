# Expansion
This directory contains any works (mine, unless otherwise mentioned) that expand on my grasp of applied statistics. This `README` file itself contains the first such works; my own look into the essence of statistics as I understand it. Other contents of this directory so far are:

- `AD`: [Approximating distributions](https://github.com/pranigopu/appliedStatistics/blob/60da65c6de1fb42cc2ffb0a1dd8523a3429d937f/expansion/approximatingDistributions.md)
  - `AD.E`: Estimators
  - `AD.LL`: Limit laws
- `HT`: [Hypothesis testing](https://github.com/pranigopu/appliedStatistics/blob/256c85409b9308a8b7989c559bf3b01b52f9f1f9/expansion/hypothesisTesting.md)
  - `HT.base`: Introduction
  - `HT.ET`: Exact tests
  - `HT.AT`: Approximate tests<br>... _extends from_ `AD`
  - `HT:GFT`: Goodness of fit tests<br>... _extends partly from_ `AD.LL`


# Understanding the essence of statistics
**_Also understanding its application in artificial intelligence_**
<br><br>
If mathematics is the science of measurement, then statistics is the mathematics of data; it is te science of measuring, i.e. quantifying different aspects of data as well as the referents and inferences that may be drawn from them. Data is the main resource in understanding a random process or a seemingly random process, i.e. a process with one or more factors that - for practical or other reasons - cannot be accounted for.

---

**NOTE**: _A process is identified as a unique process based on common factors underlying its results, outcomes or samples. Even a so-called "pure" random process is identified as a unique process based on the common factor or set of factors (known or unknown) that lead to a constant probability for any outcome._

---

Furthermore, when observing the distribution of samples from a process as frequencies of occurrence with respect to time, space or some other metrics, observing a convergence in the patterns of occurrence _suggest_ common factors that _may_ be generalised (though not yet, for certain); this is because in a random process, we except the effect of one or more of the unaccounted variables to keep changing across samples, so convergence to a pattern indicates that there are constant, universal factors (universal to all possible samples of the process) that cause these aggregate similarities despite the constant changes (at least in the long-run) in many other factors. We can try to generalise this pattern by omitting deviations from averages over time to arrive at _theoretical distributions_, which are mathematical objects that are essentially abstractions of random-process distributions of a certain kind.
<br><br>
However, statistics does not by itself grant any certainty to a process of induction; by its nature, statistics can only indicate promising leads. This is because statistics measures data, but data as such are particulars; to move from conclusions on particulars to conclusions on universals requires _conceptual integration_, i.e. the process of identifying and integrating the concepts and previous generalisations underlying a process. This is beyond the scope of statistics as such.
<br><br>
Nevertheless, knowing where to look for answers and knowing how and why the data offer promise are invaluable in the search for knowledge. Since statistics quantifies and systematises such a search, it is a vital tool in automatising learning. This points to the relevance of statistics and statistical principles in artificial intelligence (AI). AI problems, in the broadest terms, are search problems, i.e. problems requiring an automated search that starts from limited information (or even no information). In environments that are harder to generalise and thus require more experience to learn from, statistics enables us to either streamline or boil down the learning process to a (potentially) much smaller number of steps - or even a single step, in some cases - than any brute-force approach.
