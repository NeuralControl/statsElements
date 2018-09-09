Hypothesis Testing Steps
========================

Planning carefully the way we will analyze data is very important to obtain results that we can trust.

.. NOTE::
    In general, hypothesis testing requires the following steps:

    * Clearly define the problem and the hypotheses, and the type of data that will be analyzed.
    * Selecting an appropriate test and checking its assumptions.
    * If planning a study or QTP (a-priori), estimate the minimum number of samples required to obtain significance. If data is already available (post-hoc), we can estimate the power of the test on the provided data.
    * Run the test and conclude.

I. Define the problem
---------------------
The first step is to clearly define what we want to test and how we want to test it.
This step is crucial as everything else will depend on it.

We then describe the data that will be used.
There are four basic data types:

+-----------+---------------------------------------+-----------------------------------+
|           |                 Scale                 |            Categorical            |
+===========+==================+====================+==================+================+
|           |  **Continuous**  |    **Discrete**    |   **Ordinal**    |   **Nominal**  |
+-----------+------------------+--------------------+------------------+----------------+
|    Data   | takes any value  |      integers      |  obvious order   |   unordered    |
+-----------+------------------+--------------------+------------------+----------------+
|  Example  |      height      | number of children | low,medium,high  | red,green,blue |
+-----------+------------------+--------------------+------------------+----------------+


II. State the Hypotheses
-----------------------
Then we state the Null (Ho) and the Alternative Hypothesis (Ha).

Null Hypothesis (Ho)
    An hypothesis associated with a contradiction to a theory we want to prove
Alternative Hypothesis (Ha)
    An hypothesis associated with a theory we want to prove

III. Select the appropriate statistical test
------------------------------------------
We then need to choose a statistical test.

1. Tails
........

**One-sided test**
    We want to test if a parameter is inferior to a reference value or we want to test if it is superior to a reference value.
**Two-sided test**
    We want to test if a parameter doesn’t equal a reference value

2. Parametric vs Nonparametric test
...................................
Nonparametric tests do not assume that data follow a normal distribution.
We can use parametric tests on non normal data, but the statistical power of the results will be reduced
So we use a parametric test when:
- Data are normally distributed
- Sample size is large enough to satisfy the central limit theorem

.. NOTE::
    **Central Limit Theorem**
        Given certain conditions, the arithmetic mean of a sufficiently large number of iterates of independent random variables, each with a well-defined expected value and well-defined variance, will be approximately normally distributed, regardless of the underlying distribution.
 
**Parametric Tests**
    - Perform well with skewed and non normal distributions if the sample size is large enough
    - Perform well when the spread of each group is different (not always the case on nonparametric)
    - Stronger statistical power
    - For ordinal variables with seven or more categories with normal distributions it is normally advised to use parametric tests.

**Nonparametric Tests**
    - Chosen when median represents the population better than the mean (e.g. many outliers)
    - Chosen when we have a small sample size
    - Chosen when we have ordinal data, ranked data, or outliers that we can't remove

3. Choose the right test
........................
This will be described in the :ref:`statisticalTests` section

IV. Check the tests assumptions
-------------------------------
Most tests make specific assumptions on the data. Some are more sensitive to deviation from their assumptions than others.
See the :ref:`statisticalTests` section for info on specific tests. This section also shows how to visualize our data distribution against for example a normal distribution using a QQ-plot, or to test its fit.


V. Power Analysis and Statistical Power
---------------------------------------

1. State the desired :math:`{\alpha}` and :math:`{\beta}`
.........................................................

+-----------+--------------+---------------+
|           | Ho is True   | Ha is True    |
+-----------+--------------+---------------+
| Accept Ho |     good     | Type II Error |
+-----------+--------------+---------------+
| Reject Ho | Type I Error |      good     |
+-----------+--------------+---------------+

:math:`{\alpha}`, Probability of Type I error.
    This is the error when the test rejects Ho while it is actually true.
:math:`{\beta}`, Probability of Type II error
    This is the probability of not rejecting Ho when Ho is actually false.
Power, 1-:math:`{\beta}`
    Probability of correctly rejecting a False hypothesis.

.. WARNING::
    When a test outcome is not significant, it doesnt mean that Ho is True, the test is inconclusive

2. Establish the Effect Size
............................
The effect size is a measure of the strength of the effect of an independent variable on a dependant variable.
It helps assess whether a statistically significant result is meaningful.
We can use for example the :ref:`g*power` software to calculate effect size.
For reference, <0.3 is often seen as a small effect, 0.5 seen as medium and >.8 as large (Cohen).

3. Create Sampling Plan, determine sample size
..............................................
When the data is not yet available, for example when we are preparing a clinical study, we want to estimate how many samples (or subjects) we need to obtain significant results.
This is the hardest part as it often requires prior knowledge on the results.
This can come from a preliminary study, or from the literature.


VI. Run the test
----------------
Now we need to run the chosen test, estimate the test statistic, determine the p-value and conclude


Test Statistic
    Value calculated from a sample often to summarize the sample

P-value
    - Smallest level of significance that would lead to a rejection of Ho with the given data.
    - Probability of wrongly rejecting Ho. Small p-value indicates strong evidence against Ho

If p-Value is < than alpha-risk, reject Ho and accept Ha

If p-Value is > than alpha-risk, fail to reject the Null, Ho
