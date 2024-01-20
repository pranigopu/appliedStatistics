# Expansion

## Aims
This directory contains any works (mine, unless otherwise mentioned) that expand on my grasp of applied statistics. This `README` file itself contains the first such works; my own look into the essence of statistics as I understand it. In general, effective study requires three key steps: (1) conceptual mapping, wherein all the key concepts, topics and ideas are integrated hierarchically and contextually, (2) conceptual expansion, wherein certain concepts, topics or ideas are explored more deeply, as needed, and (3) practice, wherein the application of theory to more concrete examples is done. My goal here is not to summarise each and every topic I encounter, since that would often be a redundant effort after conceptual mapping and expansion, and since references are generally enough to point to definitions or brief explanations. I will focus on a selection of topics, while mapping how every topic I encounter is integrated in the broader structure of the subject.

## Conceptual map

**Quantifying probability**:

- `*.base`: Generalising & formalising probability
    - `*.base.M`: Measure<br> _Formalising probability as a kind of measure_
        - `*.base.M.PF`: Pushforward measure<br> _Applying old distributions to new transformed spaces_
    - `*.base.Math`: Mathematically detailing probability measures
        - `.base.Math.CDF`: Cumulative probability mass & the CDF function
        - `.base.Math.PDF`: Probability density & the PDF function
        - `.base.Math.topic.RETD`: Relating empirical & theoretical distributions

**Quantifying plausibility**:

- `AD`: Approximating distributions
    - `AD.E`: Estimators
    - `AD.LL`: Limit laws
- `HT`: Hypothesis testing
    - `HT.ET`: Exact tests
    - `HT.AT`: Approximate tests<br>... _extends from_ `AD`
    - `HT:GFT`: Goodness of fit tests<br>... _extends partly from_ `AD.LL`

## Understanding the essence of statistics
**_Also understanding its application in artificial intelligence_**
<br><br>
If mathematics is the science of measurement, then statistics is the mathematics of data; it is the science of measuring, i.e. quantifying different aspects of data. Data is the main resource in understanding a random process or a seemingly random process, i.e. a process with one or more factors that - for practical or other reasons - cannot be accounted for.

---

**NOTE**: _A process is identified as a unique process based on common factors underlying its results, outcomes or samples. Even a so-called "pure" random process is identified as a unique process based on the common factor or set of factors (known or unknown) that lead to a constant probability for any outcome._

---

Furthermore, when observing the distribution of samples from a process as frequencies of occurrence across time, space or some other metric, observing a convergence in the patterns of occurrence _suggest_ common factors that _may_ be generalised (though not yet, for certain); this is because in a random process, we expect the effect of one or more of the unaccounted variables to keep changing across samples, so convergence to a pattern indicates that there are constant, universal factors (universal to all possible samples of the process) that cause these aggregate similarities despite the constant changes (at least in the long-run) in many other factors. We can try to generalise this pattern by omitting deviations from averages over time to arrive at _theoretical distributions_, mathematical objects that are essentially abstractions of the observed distribution(s) of a random process or a class of random processes.
<br><br>
However, statistics does not by itself grant any certainty to a process of induction; by its nature, statistics can only indicate promising leads. This is because statistics measures data, but data as such are particulars; to move from conclusions on particulars to conclusions on universals requires _conceptual integration_, i.e. the process of identifying and integrating the concepts and previous generalisations underlying a process. This is beyond the scope of statistics as such.
<br><br>
Nevertheless, knowing where to look for answers and knowing how and why the data offer promise are invaluable in the search for knowledge. Since statistics quantifies and systematises such a search, it is a vital tool in automatising learning. This points to the relevance of statistics and statistical principles in artificial intelligence (AI). AI problems, in the broadest terms, are search problems, i.e. problems requiring an automated search that starts from limited information (or even no information). In environments that are harder to generalise and thus require more experience to learn from, statistics enables us to either streamline or boil down the learning process to a (potentially) much smaller number of steps than any brute-force approach, or even a single step in some cases.
