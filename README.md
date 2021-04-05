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


#### Outcomes vs School Size


#### Outcomes vs School Spending (Per Student)


#### Outcomes vs School Type


### Differences?

Bulleted list addressing how each of the seven school district metrics was affected by the changes in the data

- How is the district summary affected?
- How is the school summary affected?
- How does replacing the ninth graders' math and reading scores affect Thomas High School's performance relative to the other schools?
- How does replacing the ninth-grade scores affect:
  - Math and reading scores by grade
  - Scores by school spending
  - Scores by school size
  - Scores by school type


## Summary
Summarize 4 major changes in the updated school district analysis after removing the reading and math scores for the ninth-grade at Thomas High School


### Note
Must have:
- Title and multiple sections
- Each section has a heading and subheading
- Links to images which work/Code formatted correctly

