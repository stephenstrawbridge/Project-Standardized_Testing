# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Test Analysis

### Overview
The SAT and ACT are standardized tests that many colleges and universities in California (United States) have required for their admissions process since the 1940’s.  A student’s score on these standardized tests, in addition to grade point average (GPA), and essay responses, are used to evaluate the academic merit of college applicants and for extending a potential offer of admission.

How standardized can these tests truly be?  That is, can every student have an equal chance of succeeding on these tests? It turns out, these tests can have some “unstandardized” qualities.  

In December of 2019, students and educators commenced a lawsuit over the University of California over its use of standardized tests, claiming these exams were “discriminating against applicants of color from low-income families by requiring standardized tests” ([*source*](https://www.nbcnews.com/news/education/california-lawsuit-blasts-sat-act-exams-discriminatory-n1099416)).   Commencement of this lawsuit was a long time coming, as most opposers of standardized tests have shared this sentiment for at least a couple decades.  Preparing for these exams can be costly, as preparation programs for these tests can be several hundred, or even several thousand dollars ([*source*](https://blog.prepscholar.com/how-much-do-sat-prep-courses-cost)).  Some school districts, as compared to others, have distinct classes SAT/ACT prep classes offered to students.  

Given these conditions, many California citizens claim that access and opportunity to best prepare for the tests is far from equal among the California high school student population.  Some citizens argue it is the test administrators responsibility to ensure resources are allocated proportionally to ensure more equal opportunity.


## Problem Statement
We hypothesize that although the high school student population of California has a vastly wide range of demographics, the participating and successful standardized test takers of that population may not be as diverse.  This project aims to analyze standardized test participation and success rates among the specific demographic of school county, which could be indicative of further demographics within those counties, and allocate resources as necessary to ensure a more equal representation of successful standardized test takers.

## Data Dictionary
|Feature|Type|Dataset|Description|
|---|---|---|---|
|**school**|*object*|CA 2019 SAT/ACT Data|Every public school in California.| 
|**district**|*object*|CA 2019 SAT/ACT Data|Every public school district in California.| 
|**county**|*object*|CA 2019 SAT/ACT Data|Every county, for every public school in California.| 
|**enroll_12_x**|*int*|CA 2019 SAT/ACT Data|The number of enrolled 12th graders per school.|
|**sat_num_takers_12**|*int*|CA 2019 SAT Data|The number of enrolled 12th graders per school take took the SAT exam.|
|**enroll_11**|*int*|CA 2019 SAT/ACT Data|The number of enrolled 11th graders per school.|
|**sat_num_takers_11**|*int*|CA 2019 SAT Data|The number of enrolled 11th graders per school take took the SAT exam.|
|**sat_benchmark_12**|*int*|CA 2019 SAT Data|The number of enrolled 12th graders per school take took the SAT exam who reached, or exceeded, the standard benchmark score for 2019.|
|**sat_percent_12**|*float*|CA 2019 SAT Data|The number of enrolled 12th graders per school take took the SAT exam who reached, or exceeded, the standard benchmark score for 2019 divided by the total number of 12th graders per school who took the SAT.|
|**sat_benchmark_11**|*int*|CA 2019 SAT Data|The number of enrolled 11th graders per school take took the SAT exam who reached, or exceeded, the standard benchmark score for 2019.|
|**sat_percent_11**|*float*|CA 2019 SAT Data|The number of enrolled 11th graders per school take took the SAT exam who reached, or exceeded, the standard benchmark score for 2019 divided by the total number of 11th graders per school who took the SAT.|
|**act_num_takers_12**|*int*|CA 2019 ACT Data|The number of enrolled 12th graders per school take took the ACT exam.|
|**act_avg_score_read**|*int*|CA 2019 ACT Data|The average score on the Reading section of the ACT among 12th graders take took the ACT exam per school.|
|**act_avg_score_eng**|*int*|CA 2019 ACT Data|The average score on the English section of the ACT among 12th graders take took the ACT exam per school.|
|**act_avg_score_math**|*int*|CA 2019 ACT Data|The average score on the Math section of the ACT among 12th graders take took the ACT exam per school.|
|**act_avg_score_sci**|*int*|CA 2019 ACT Data|The average score on the Science section of the ACT among 12th graders take took the ACT exam per school.|
|**act_num_above_benchmark**|*int*|CA 2019 ACT Data|The number of enrolled 12th graders per school take took the ACT exam who reached, or exceeded, the standard benchmark score for 2019.|
|**act_percent_above_benchmark**|*float*|CA 2019 ACT Data|The number of enrolled 12th graders per school take took the ACT exam who reached, or exceeded, the standard benchmark score for 2019 divided by the total number of 12th graders per school who took the ACT.|

## Summary of Analysis
In terms of numbers on average, the counties of Modoc, Sierra, and Trinity had the lowest SAT participation for both 11th and 12th grades.  11th grade participation ranged from about 10 to 30 students, while 12th grade participation ranged from about 5 to 10 students.  Even considering the fact that these counties may have a smaller population size, these stats were far below the average of all schools, where the 11th grade and 12th grade means were about 119 students and 100 students, respectively. 

In terms of numbers on average, the counties of Sierra, Del Norte, and Plumas had the lowest ACT participation for 12th grade.  Participation ranged from only 3 to 9 students, with the average in comparison at 48 students.  

In terms of percentages on average, the counties of Modoc, Sierra, and Inyo had the lowest percentage of students meet or exceed the SAT score benchmark for the 11th grade.  For the 12th grade, the counties were Trinity, Colusa, and Modoc.  The average percentage across all schools, for both grades, was about 37% to 32%. 

One key takeaway from these findings is that fact that nearly all of the highly urbanized areas of California were excluded from these bottom 10 ranks.  Nearly all of the counties present in the findings above are located in more rural areas.

Grouping and summary statistic syntax was referenced using the following source: ([*source*](https://stackoverflow.com/questions/20069009/pandas-get-topmost-n-records-within-each-group)).

The datasets provided, as analyzed further on in the project, cast insight into standardized test score results among different school districts and their respective geographical regions.  Within these regions, further research can show the racial and income demographics of the regions (for example: if the county of Mendocino is a low performing county, we can find the racial and income demographics within Mendocino).  In the section below, we seek to cast insight into these more specific demographics to corroborate our findings in the provided datasets.

*Racial Demographics*:
According to the 2020 SAT Collegeboard annual report ([*source*](https://reports.collegeboard.org/pdf/2020-california-sat-suite-assessments-annual-report.pdf)), Asian and White students scored the highest, with a mean score for Asian students at 1207 and a mean score for White students at 1158.  The lowest performing demographics were American Indian and African American students, with mean scores of 917 and 938, respectively.  One other important finding from this report is that Hispanic/Latino students had the largest number of test takers, by a huge margin, with over 140,000 students while the next highest participation was White students with around 57,000 students.  Hispanic/Latino students on average still performed significantly below White/Asian students, with a mean total score of 962.

*Income Demographics*:
According to the National Center for Education Statistics (NCES) ([*source*](https://nces.ed.gov/programs/digest/d12/tables/dt12_173.asp)), in their data pulled from 2010 through 2012, family income and highest level of parental education were directly correlated with student scores.  In every income bracket given, the higher the family income, the higher the student’s score on average.  For parental education, the same effect is seen (higher level of education, higher student score on average).  

*Location/Geography Demographics*:
Lastly, and perhaps most importantly, we can see both SAT and ACT score reports based on geographical region by utilizing an interactive online map created by EdGAP.org (insert source).  We can see that many urbanized areas have a wide range of average scores, while more rural areas tend to have lower than average scores ([*source*](https://www.edgap.org/?gclid=Cj0KCQjwlvT8BRDeARIsAACRFiVWj0oUKt_gC13oDvrnZkDeJTNtvK0TzDHaDbVdKt1kMR9sVUPDhi0aAvwXEALw_wcB#9/37.4548/-121.6736)).


## Conclusions and Recommendations
*Recap*: The initial goal of the data analysis was to obtain insight into the specific demographics of low performing students, from a location perspective and then a racial and income persepctive.  Our insight was obtained in the following manners:

*Dataset Research*:  Based on our dataset research, slightly compelling trends were seen from comparing the grade size to the number, and percentage, of students who passed the standardized benchmark for the ACT and SAT.  Additionally, when grouping by the top 10 lowest performing counties for each grade and test, it was observed that many of these counties were in less urbanized areas.  

*Outside Research*:  After gaining insight into which counties had lower performing students, we could gain insight into the specific counties demographics.  Rural areas tended to be predominantly the races of White, Hispanic, and Native American.  This finding was fairly aligned with the racial demographics that stated that Native Americans were the lowest performing racial group.  From an income perspective, the rural areas also had the lowest level of parental income, which aligns with the findings that parental income is positively correlated with student performance.

*Key Takeaways, Recommendations, and Limitations*:  A main takeaway from these findings is that school size has a slightly, but not strong, correlation to student performance on exams.  After diving deeper into more specific demographics from outside research, it is apparent that many other factors must be taken into consideration.  For example, urban counties such as Los Angeles, have a high student population but may have a very fluctuating range of low and high performing students within the county.  One inherent limitation of this project is that although it was found that rural counties perform more poorly as compared to urban counties on average, greater research into urban counties is needed to compartmentalize high and low performing students.  Overall, as a data scientist presenting to the college board, my recommendation is to allocate more funding and education centers in these rural counties for which standardized test participation is lower.  For urban areas, my recommendation is to have allocate funding not per location, but rather per income demographic. 
