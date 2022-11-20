
# SAT&ACT Test Analysis 
**By Thanapong (billy)**


This project start with the examine the fundamental of standadized test in United State. The aiming of the project was to uncover the pattern on how the standadized test has been choosing in order to suggest/giving an idea on how to choose the test. 

This analysis base on 2 assumption:   
- student only could take a test in their state and use it as an enroll on that state.
- college located in the state will be representative of the state



## DATA


- [act_2017.csv](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows): 2017 ACT Scores by State
- [sat_2017.csv](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/): 2017 SAT Scores by State
- [sat_act_by_college](https://www.compassprep.com/college-profiles/).csv: Ranges of Accepted ACT & SAT Student Scores by Colleges
- [stateabb.csv](https://worldpopulationreview.com/states/state-abbreviations) : the state abbreviation of United states
- [cwurData.csv](https://github.com/arnaudbenard/university-ranking/blob/master/cwurData.csv) : the ranking of college



## Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
 |college|object|college| the name of the college in each state
 |accept rate |float64 | sat_act_by_college| the rate of acceptance in each college
 |sat 25%|float64| sat_act_by_college|the score of 25 percentile in SAT test in each college
 |sat 75% |float64|sat_act_by_college| the score of 75 percentile in SAT test in each college
 |act 25%|float64| sat_act_by_college|the score of 25 percentile in ACT test in each college
 |act 75%|float64|sat_act_by_college| the score of 75 percentile in ACT test in each college
 |abrev. |object|stateabb|the short name of the state
 |code | object|stateabb|the code name of the state
 |rank | int64|rank|the ranking of college
 |State	|object | ACT/SAT| State
 |Participation|object|ACT/SAT|the percentage of people who participate the test
  |	Math	|float64|ACT/SAT | the average score of the subject 
 |	English|float64|ACT| the average score of the subject 
 |Reading	|float64|ACT | the average score of the subject 
 |Science	|float64|ACT | the average score of the subject 
 |Composite|object|ACT|the average of  four test scores
 |EBRW| int64| SAT | Evidence-Based Reading and Writing
 |Total | int64 | SAT |the summation of two sections score

## Conclusions

Due to the limit of time on this analysis, the result of this analysis should be only an additional component for decision-making on how to choose the test to enroll in. From the analysis of the 2017 SAT & ACT databases, the participation in SAT and ACT in each state has been explored. The proportion of both tests varied by each state, and the result showed that the correlation of SAT participation and ACT participation is negatively correlated, which means in each state, students might consider taking only one test. However, we can separate these states into two groups. The first group includes the states with the high proportion in one test, which will be defined as a "pure state", and the other group is the state with the mixing in proportion of both tests, which will be defined as an "ambigious state'.

The score range acceped of ACT & SAT has been extract at 75 percentiles score and using z-score to standadized the score and compare together in each college. According to the result of comparing the scores, some states have SAT scores higher than ACT scores at the same 75 percentiles, some states show the result conversely, and some show that both scores are approximately equal. After seeing the relation between these differences in scores and the ranking of the college. Therefore, we can divide the ambigious state into 3 sub-groups, which are : 1. High rank college (SAT > ACT) with the ranking > 52       
2. Middle rank college (ACT = SAT) 3. Low rank college (ACT> SAT) with the ranking < 100

These 3 groups have been used to analyze the relationship between the participation rate on both tests and the ranking of the college. Then we found that most students who enroll in a high-ranking college will participate in the SAT test. On the other hand, most students who participate in the ACT test will enroll in a low-ranking college. Furthermore, I have analyzed the relationship between participation rate and mean score of both tests by each state, and we have seen that the more participation in each test, the lower the mean score.

From the analysis, I would suggest that the state with a low-ranked college should take an ACT test, but the state with a high-ranked college should take the SAT test. A student in a state with a middle ranking could take either test. Nevertheless, this project is an initial step of analysis for giving an idea on decision making. Discretion is still required, along with the test taker's own academic aptitude, to make decisions.


