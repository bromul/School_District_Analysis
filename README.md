# PyCitySchools with Pandas

## Overview
This project analyzed school and student data to determine the relationships between funding, size, etc., and grade outcomes.

### Purpose

We have been asked by Maria, the Chief Data Scientist for the City school district, to help analyze data on school funding and its effects on the standardized testing of students. We were given 2 datasets - one with metrics for each school in the district, and one with data on individual students. 

The only issue we noticed with the data was that some students had titles before and/or after their names - something that was easily fixed with a couple lines of code.

We were then tasked with providing the district with a high level snapshot of the district's key metrics, an overview of key metrics for each school within the district, and mulitipe tables which presented the top 5 best and worst performing schools, the average math and reading scores for each grade in each school, and general school performance as based on a school's budget per student, size, and the type of school (District or Charter). 

Unfortunately, once we had completed our initial analysis, it was brought to our attention that the 9th graders at Thomas High School likely had their grades altered. Although the school board was still unsure of the extent of the academic dishonesty at the time, we were tasked with removing the grades from the 9th graders at Thomas High School and rerunning our analysis to uphold state-testing standards. 


## Results

### Initial Results

#### District Summary
During our initial investigation we found:
  - District Summary:
    - Total Students: 39,170
    - Total Budget: $24,649,428.00
    - Average Math Score: 79.0%
    - Average Reading Score: 81.9%
    - Percent Passing Math: 75%
    - Percent Passing Reading: 86%
    - Overall Passing: 65%

You can see this summary below:

![District Summary (Initial)](https://github.com/bromul/School_District_Analysis/blob/main/Resources/Pre%20NAN/district_summary_pre_nan.PNG)


#### Top and Bottom Performing Schools

From here, we split the district into its constituent schools and ranked them based on overall passing rates. As we can see with the picture below, the top 5 schools by overall passing rate are all smaller, charter schools: 

![Top Performing Schools (Initial)](https://github.com/bromul/School_District_Analysis/blob/main/Resources/Pre%20NAN/top_schools_pre_nan.PNG)

On the other hand, the bottom 5 schools by overall passing rate are all larger, district schools:

![Bottom Performing Schools (Initial)](https://github.com/bromul/School_District_Analysis/blob/main/Resources/Pre%20NAN/bottom_schools_pre_nan.PNG)


#### Outcomes vs School Size

To expand our analysis further, we then looked into the relationships between school spending per student, school size, and school type. This allowed us a deeper look into school outcomes and their causes.

We first categorized each school into bins of either Small (<1000), Medium (1000-2000), or Large (2000-5000). This allowed us to determine the relationship between school size and the percentage of students who passed both reading and math. Unsurprisingly, larger school sizes are correlated with lower outcomes. This is most stark when looking at the overall passing percentage, which drops from ~90% to ~58% when school populations are large:

![Outcomes by School Size (Initial)](https://github.com/bromul/School_District_Analysis/blob/main/Resources/Pre%20NAN/avg_passing_by_size_pre_nan.PNG)

This highly suggests that smalle populations are more conducive to education and standardized testing.


#### Outcomes vs School Spending (Per Student)

Once we finished up that analysis, we proceeded to look into the relationship between school spending (per student) and testing outcomes. Contrary to what we initially assumed, this relationship appears to be inverse. That is, the average math and reading scores, as well as the overall passing rate, falls as the amount spent per student increases:

![Outcomes by School Spending Per Student (Initial)](https://github.com/bromul/School_District_Analysis/blob/main/Resources/Pre%20NAN/avg_passing_by_spending_pre_nan.PNG)

This eschews the conventional wisdom that educational outcomes can be attained by throwing money at the issue, which is to say, larger budgets don't correlate with greater outcomes. This suggests that targetting money and using it more efficiently can lead to greater outcomes.


#### Outcomes vs School Type

Finally, we analyzed school outcomes by the type of school (District or Charter). Much as when we looked at the top and bottom performing schools, Charter schools have a better passing rate for both math and reading:

![Outcomes by School Type (Initial)](https://github.com/bromul/School_District_Analysis/blob/main/Resources/Pre%20NAN/avg_passing_by_type_pre_nan.PNG)

This may suggest that charter schools are more effective than district schools at producing positive outcomes with standardized testing. However, before any major conclusions can be drawn, it's important to note that some of the variables may be confounding. Specifically, school size may possibly be the primary driver of testing outcomes, e.g., smaller class sizes leads to more personalized instruction which in turn leads to better outcomes. If that's the case, the charter schools may not have better outcomes because they're charter schools, per se, but because charter schools have the funding and ability to limit class sizes. More research and analysis would be needed to come to a conclusion either way, but the solution to the problems facing district schools highly depends on interrogating these issues.
 


### Post-Changes Results

#### District Summary

Once we had performed our initial analysis, we were alerted to potential issues of academic dishonesty with 9th graders at Thomas High School. Due to this, we re-ran our analysis without their scores. These are the updated results:

  - District Summary:
    - Total Schools: 15
    - Total Students: 39,170
    - Total Budget: $24,649,428.00
    - Average Math Score: 78.9%
    - Average Reading Score: 81.9%
    - Percent Passing Math:  74.8%
    - Percent Passing Reading: 85.7%
    - Overall Passing: 64.9%

You can see this summary below:

![District Summary (Post-Changes)](https://github.com/bromul/School_District_Analysis/blob/main/Resources/Post%20NAN/district_summary_post_nan.PNG)


#### Top and Bottom Performing School

Again, we proceeded to split the district into its constituent schools and find the best:


![Top Performing Schools (Post-Changes)](https://github.com/bromul/School_District_Analysis/blob/main/Resources/Post%20NAN/top_schools_post_nan.PNG)


and worst performing schools:

![Bottom Performing Schools (Post-Changes)](https://github.com/bromul/School_District_Analysis/blob/main/Resources/Post%20NAN/bottom_schools_post_nan.PNG)

Interestingly, despite the changes we made lowering Thomas High School's overall passing percentage, removing the 9th graders' grades _did not_ affect the school rankings. This is to say, although there are slight differences in the calculated statistics, the Thomas High School is still the second best school in terms of overall passing percentages. This is also true for the worst performing schools, who did not move up or down the rankings either. 

#### Outcomes vs School Size

Although we removed the 9th graders from Thomas High School's calculations, the trend between school size and testing outcomes did not greatly change either:

![Outcomes by School Size (Post-Changes)](https://github.com/bromul/School_District_Analysis/blob/main/Resources/Post%20NAN/avg_passing_by_size_post_nan.PNG)

There is still a negative correlation between school size and the overall passing rate. 

#### Outcomes vs School Spending (Per Student)

Additionally, we did not see any major changes between the relationship between a school's spending per student and the overall passing rate with the removal of Thomas High School's 9th graders:

![Outcomes by School Spending Per Student (Post-Changes)](https://github.com/bromul/School_District_Analysis/blob/main/Resources/Post%20NAN/avg_passing_by_spending_post_nan.PNG)


#### Outcomes vs School Type

Finally, the same can be said for the correlation between school type and overall passing rates. Despite Thomas High School being a charter school, taking away the potentially inflated grades did not reverse the trend we had seen previously:

![Outcomes by School Type (Post-Changes)](https://github.com/bromul/School_District_Analysis/blob/main/Resources/Post%20NAN/avg_passing_by_type_post_nan.PNG)


### Differences Between the Initial and Secondary Analyses

Although major trends did not change or reverse with the dismissal of grades from Thomas High School's 9th graders, there were still differences between the two datasets that should be noted:


-  Overall the District Summary scores generally stayed the same. However, there were slight differences:
  - Average Math Score: 
    - Initial: 79%
    - Post-Changes: 78.9%
  - Percent Passing Math:
    - Initial: 75%
    - Post-Changes: 74.8%
  - Percent Passing Reading:
    - Initial: 86%
    - Post-Changes: 85.7%
  - Overall Passing:
    - Initial: 65%
    - Post-Changes: 64.9%   
- Despite Thomas High School's overall passing rate dropping from ~90.95% to ~90.63%, it maintained its position as the second best performing school.
  - Interestingly, however, while most of Thomas High School's average scores and passing percentages slightly dropped with the removal of the 9th graders, its average reading score actually increased, from ~83.85% to ~83.9%.
- Further, we found that the removal of the 9th graders from Thomas High School had a minimal effect on:
  - Scores by School Spending
    - Scores remained relatively stable whether or not we removed the 9th graders from Thomas High School from our analysis. This is true of both the scores themselves and the trends they revealed.
  - Scores by School Size
    -  Scores remained relatively stable whether or not we removed the 9th graders from Thomas High School from our analysis. This is true of both the scores themselves and the trends they revealed.
  - Scores by School Type
    - Scores remained relatively stable whether or not we removed the 9th graders from Thomas High School from our analysis. This is true of both the scores themselves and the trends they revealed.
  - Math and reading scores by grade
    - Scores remained relatively stable whether or not we removed the 9th graders from Thomas High School from our analysis. This is true of both the scores themselves and the trends they revealed. The only major difference is that, in the second analysis, 9th graders at Thomas High School have their average grade replaced with NAN.

We can see this clearly by comparing the _intial_ math and reading averages across grade levels:

![Average Math Scores By Grade (Initial)](https://github.com/bromul/School_District_Analysis/blob/main/Resources/Pre%20NAN/avg_math_score_by_grade_pre_nan.PNG) ![Average Reading Scores By Grade (Initial)](https://github.com/bromul/School_District_Analysis/blob/main/Resources/Pre%20NAN/avg_reading_score_by_grade_pre_nan.PNG)

with the math and reading averages across grade levels without the 9th graders:

![Average Math Scores By Grade (Post-Changes)](https://github.com/bromul/School_District_Analysis/blob/main/Resources/Post%20NAN/avge_math_score_by_grade_post_nan.PNG) ![Average Reading Scores By Grade (Post-Changes)](https://github.com/bromul/School_District_Analysis/blob/main/Resources/Post%20NAN/avg_reading_score_by_grade_post_nan.PNG)


## Summary
To summarize, although much of our analysis did not differ with the removal of the 9th grade math and reading scores for Thomas High School, there were a few changes that should be noted, including, but not limited to:

- The District Summary. Overall, removing the 9th grade math and reading scores lead to a slight decrease in district-wide metrics - showing slightly lower grade averages and passing rates.
- Thomas High School Overall Passing Rate. Thomas High School had about a .3% decrease in its overall passing rate, i.e., students who passed both math and reading.
- Thomas High School Metrics. The average math score, the percent who passed math, and the percent who passed reading all slightly declined by about .05%, .09%, and .3%, respectively. This was to be expected if the 9th graders at Thomas High School had participated in academic dishonesty.
- Thomas High School Average Reading Score. With the removal of it 9th grade math and reading scores, as previously noted, most metrics for Thomas High School dropped slightly. Surprisingly, however, we found that Thomas High School's average reading score went slightly up by about .04%. This bucks the established trend we've found and may merit further investigation into why that's the case.  
