Hypothesis Testing Steps
==================


1. Define the Problem
---------------------
The first step is to clearly define what we want to test and how we want to test it
We then clearly define the data that will be used.
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


2. State the Hypotheses
-----------------------
Then we state the Null (Ho) and the Alternative Hypothesis (Ha)

- Null Hypothesis (Ho): An hypothesis associated with a contradiction to a theory we want to prove
- Alternative Hypothesis (Ha): An hypothesis associated with a theory we want to prove

3. Select the appropriate statistical test
------------------------------------------
We then need to choose a statistical test.
a. Tails
........
**one-sided test**: We want to test if a parameter is inferior to a reference value
or we want to test if it is superior to a reference value.

**two-sided test**: We want to test if a parameter doesn’t equal a reference value

b. Parametric vs Nonparametric test
...................................
Nonparametric tests do not assume that data follow a normal distribution.
We can use parametric tests on non normal data, but the statistical power of the results will be reduced
So we use a parametric test when:
- Data are normally distributed
- Sample size is large enough to satisfy the central limit theorem

.. NOTE::
    **Central Limit Theorem**:

    Given certain conditions, the arithmetic mean of a sufficiently large number of iterates of independent random variables, each with a well-defined expected value and well-defined variance, will be approximately normally distributed, regardless of the underlying distribution.
 
**Parametric Tests**
    - Perform well with skewed and non normal distributions if the sample size is large enough
    - Perform well when the spread of each group is different (not always the case on nonparametric)
    - Stronger statistical power

**Nonparametric Tests**
    - Chosen when median represents the population better than the mean (e.g. many outliers)
    - Chosen when we have a small sample size
    - Chosen when we have ordinal data, ranked data, or outliers that we can't remove

4. State the desired Alpha and Beta
-----------------------------------

+-----------+--------------+---------------+
|           | H0 is True   | Ha is True    |
+-----------+--------------+---------------+
| Accept H0 | good         | Type II Error |
+-----------+--------------+---------------+
| Reject H0 | Type I Error | good          |
+-----------+--------------+---------------+

Alpha, Significance level
    Probability of type I error


Establish the Effect Size
-------------------------
asd

Create Sampling Plan, determine sample size
-------------------------------------------
asd

Collect and record data
-----------------------
asd

Check the tests assumptions, Normality plot
-------------------------------------------
asd

Calculate the test statistic
----------------------------
- Test Statistic: Value calculated from a sample often to summarize the sample


Determine the p-value
---------------------
P-value
    - Smallest level of significance that would lead to a rejection of Ho with the given data.
    - Probability of wrongly rejecting Ho. Small p-value indicates strong evidence against Ho

If p-Value is < than alpha-risk, reject Ho and accept Ha

If p-Value is > than alpha-risk, fail to reject the Null, Ho
