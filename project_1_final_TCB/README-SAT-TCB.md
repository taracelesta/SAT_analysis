# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Test Analysis


### Introduction

The SAT and ACT are standardized tests that many colleges and universities in the United States require for their admissions process. This score is used along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university.

The SAT has two sections of the test: Evidence-Based Reading and Writing and Math ([*source*](https://www.princetonreview.com/college/sat-sections)). The ACT has 4 sections: English, Mathematics, Reading, and Science, with an additional optional writing section ([*source*](https://www.act.org/content/act/en/products-and-services/the-act/scores/understanding-your-scores.html)). They have different score ranges, which you can read more about on their websites or additional outside sources (a quick Google search will help you understand the scores for each test):
* [SAT](https://collegereadiness.collegeboard.org/sat)
* [ACT](https://www.act.org/content/act/en.html)

Standardized tests have long been a controversial topic for students, administrators, and legislators. Since the 1940's, an increasing number of colleges have been using scores from sudents' performances on tests like the SAT and the ACT as a measure for college readiness and aptitude ([*source*](https://www.minotdailynews.com/news/local-news/2017/04/a-brief-history-of-the-sat-and-act/)). Supporters of these tests argue that these scores can be used as an objective measure to determine college admittance. Opponents of these tests claim that these tests are not accurate measures of students potential or ability and serve as an inequitable barrier to entry.


### Problem Statement

I am a Diversity, Equity & Inclusion Analysist for College Board. I am presenting to the board members of College Board who make decisions for the SAT test as it applies to the state of Colorado.

Our SAT test is criticized as being a tool that creates racial disparity. This critique stems from the idea that our exam gives an unfair advantage to students who attend white-majority schools. 

This project aims to identify, at the Colorado state level, the differences in participation rates and test scores of students by their race. 

From this information, CollegeBoard can improved funding decisions to ensure that our test is BIPOC inclusive. Achieving this inclusivity will allow us to achieve our mission of providing a fair measurement of success for all students.


### Methodology

For this project, I analyzed aggregate SAT scores and participation rates for the state of Colorado. I found this data from the Colorado Department of Education's website. Through this analysis, I used Python to identify trends to address my problem statement.


### Findings

SAT attendance rates by races were very similar. The majority of races and student population (black, white, hispanic, 2 or more races) fell within a max of only .82% from each other. The largest percentage diference were between Asian and Natice American students, with Native American students attending 9.4% less than Asian students.

The largest 11th grade student populations in Colorado are by far white and hispanic. White students totaled 33,958 and hispanic students totaled 20,454.

However hispanic students score on average 112.2 points less on their SATs than their white peers.

Native American students score on average 250.75 points less than their Asian peers, which is the largest difference in SAT scores seen in Colorado.

Black students score on average 50 points better than Native American students.

The lowest scoring students in Colorado are Native American(852), Black(902), and Hispanic(909).
The highest scoring students in Colorado are White(1021), Asian(1103), and students who are 2 or more races(1037).


### Conclusion & Reccomendations

The SAT's racial achievement gap is a reflection of the racial inequities in our society as a whole. Reconciling this gap will lead to equalizing educational opportunities and is one way to dissimilate inequality. 

Now that we know SAT scores hold a racial bias, we must hypothesize the reasons behind this.

Once we discover the “why’s” behind this disparity, we can create appropriate programs and allocate funding properly to help solve this problem.


### Possible Items to Further Investigate:

* What makes a student test better?
    - Take the SAT test more than once get better scores?
    - What test Prep are these students using?
    - How are these items available to students across races?
* Do wealthier students get higher SAT scores? 
    - Is this because of  tutoring costs?
    - Is this because of testing costs?
* Do wealthier school districts get better Scores?
    - Gifted and Talented programs avalible
    - A/P courses avalible
    - Test prep classes available
* Drop out, suspension, unaddressed emotional/behavioral disorders?
* Who writes the SAT tests? Are the questions biases towards more affluent students?


### Datasets

* [`sat_2019.csv`](./data/sat_2019.csv): 2019 SAT Scores by State ([source](https://blog.prepscholar.com/average-sat-scores-by-state-most-recent))
* [`sat_2019_co.csv`](./data/2019_P_SAT_CO_District_Results.csv): 2019 SAT Scores in Colorado by District ([source](https://www.cde.state.co.us/assessment/sat-psat-data/)
* [`sat_2019_co_race.csv`](./data/2019_P_SAT_Scores_Race.csv): 2019 SAT Scores in Colorado by Race ([source](https://www.cde.state.co.us/assessment/sat-psat-data/)


### Data Dictionary


**Colorado SAT District and School Achievement Results** 

|Feature|Type|Dataset|Description|
|---|---|---|---|
|district_name|onject|co_school_scores|Name of school district|
|total_student_count|float64|co_school_scores|Amount of grade 11 enrolled students|  
|participation_rate|float64|co_school_scores|Percentage of student who took test|
|total|float64|co_school_scores|Total SAT scores|
|evidence_based_reading_writing|float64|co_school_scores|Evidence Based Reading and Writing section score|
|math|float64|co_school_scores|Math section score|


**Colorado SAT Disaggregated District and School Achievement Results By Race**  

|Feature|Type|Dataset|Description|
|---|---|---|---|
|district_name|object|by_race_co_scores|Name of school district|
|race/ethnicity|object|by_race_co_scores|Race/Ethnicity of student|
|total_student_count|float64|by_race_co_scores|Amount of grade 11 enrolled students|  
|participation_rate|float64|by_race_co_scores|Percentage of student who took test|
|total|float64|by_race_co_scores|Total SAT scores|
|evidence_based_reading_writing|float64|by_race_co_scores|Evidence Based Reading and Writing section score|
|math|float64|by_race_co_scores|Math section score|


**National SAT Disaggregated District and School Achievement Results By State**  

|Feature|Type|Dataset|Description|
|---|---|---|---|
|state|object|by_state_scores|SAT data from specific state|
|evidence_based_reading_writing|int64|by_state_scores|Evidence Based Reading and Writing section score|
|math|int64|by_state_scores|Math section score
|total|float64|by_race_co_scores|Total SAT scores|
|participation_rate|int64|by_state_scores|Percentage of student who took test|

