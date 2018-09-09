Examples of Statistical Inference
=================================

.. _teacherReputation:
Influence of Teacher Reputation on Rating
-----------------------------------------
From onlinestatbook

Questions:
    - Does an instructor's prior reputation affect student rating?
    - Does the size of this effect depend on student characteristics?

Experimental Design:
    - subjects viewed video of a lecture of a teacher after reading an evaluation of the instructor, then they rated the instructor.
    - subjects where randomly assigned two conditions: Charismatic (reading a good evaluation), Punitive (reading a bad review of the instructor)

Descriptive Statistics:
    - Boxplot showing the student rating vs the two conditions. Ratings seem higher for the charismatic teacher.
    - N, Mean, Median, Skewness, Kurtosis etc are calculated for both conditions

Inferential Statistics:
    - Independent samples t-test used to test the differences. The result is significant, supporting the conclusion that instructor reputation affects ratings.
    - Assumptions:
        - Each score is sampled independently and randomly: Ok, as the students are randomly assigned to a condition.
        - Normal distribution of the scores within each condition: Violated to a moderate degree because of the skewness.
        They assessed that this was not important using the data analysis lab.
        - Equality of variance between the two populations: Ok

Mediterranean Diet and Health
-----------------------------
From onlinestatbook

Question:
    - Is a mediterranean diet healthier than a diet with high-saturated fat?

Experimental Design:
    - 605 survivors of a heart attack assigned to either the AHA diet or the Mediterranean diet
    - Over a 4 year period, patients following the Mediterranean diet were seen initially, then after two months, then once a year to check observance.
    - The other group was assumed to follow the diet.
    - Information was collected on number of deaths from cardiovascular causes, non fatal heart-related episodes and tumors.

Descriptive Statistics:
    - Histogram, frequencies tables. 20% of the AHA diet patients had at least one illness, compared to 10% on the Mediterranean.

Inferential Statistics:
    - A Chi-Square test can be used to check if there is a relationship between diet and outcome..
    - Conclusion that outcome is related to diet and that Mediterranean diet is superior to the AHA diet.

Who is buying iMacs
-------------------
From onlinestatbook

Question:
    - Are the buyers of the latest Mac new buyers, or did they previously have a Mac product

Experimental design:
    - They asked 500 of the new Mac purchasers if they owned or had owned a Mac
Results:
    - 83 new computer owners, 60 who had a Windows computer, 357 who had owned a Mac
    - Proportion of first time computer owners = 0.167.
    - The 95% confidence interval on the proportion is calculated ( 0.13<CI<.20 ) therefore, it is likely that between 13% and 20% of new Mac buyers are first time computer owners.
Assumptions:
    - No reason seen that would violate the assumptions of normality or independence.
Epilog:
    - After one year, Apple reports that 1/3 of new buyers are first time computer buyers. This is outside the CI range. Is this a sampling error ? Other factors?




