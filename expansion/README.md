# Expansion

## Aims
This directory contains any works (mine, unless otherwise mentioned) that expand on my grasp of applied statistics. In general, effective study requires three key steps: (1) conceptual mapping, wherein all the key concepts, topics and ideas are integrated hierarchically and contextually, (2) conceptual expansion, wherein certain concepts, topics or ideas are explored more deeply, as needed, and (3) practice, wherein the application of theory to more concrete examples is done. My goal here is not to summarise each and every topic I encounter, since that would often be a redundant effort after conceptual mapping and expansion, and since references are generally enough to point to definitions or brief explanations. I will focus on a selection of topics, while mapping how every topic I encounter is integrated in the broader structure of the subject.

## Conceptual map

**Quantifying probability**:

- `*.base`: Generalising & formalising probability
    - `*.base.M`: Measure<br> _Formalising probability as a kind of measure_
        - `*.base.M.PF`: Pushforward measure<br> _Applying old distributions to new transformed spaces_
    - `*.base.Math`: Mathematically detailing probability measures
        - `*.base.Math.CDF`: Cumulative probability mass & the CDF function
        - `*.base.Math.PDF`: Probability density & the PDF function
        - `*.base.Math.topic.RETD`: Relating empirical & theoretical distributions

**Quantifying plausibility**:

- `AD`: Approximating distributions
    - `AD.E`: Estimators
    - `AD.LL`: Limit laws
- `HT`: Hypothesis testing
    - `HT.ET`: Exact tests
    - `HT.AT`: Approximate tests<br>... _extends from_ `AD`
    - `HT:GFT`: Goodness of fit tests<br>... _extends partly from_ `AD.LL`
