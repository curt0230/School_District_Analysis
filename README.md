# School_District_Analysis
## Project overview
The purpose of this project was to analyze the impact of several metrics (student body size, per-capita spending, and school type (district or charter)) on reading and math scores and passing rates across the district.  Since the school board has received evidence of tampering regarding 9th grade reading and math scores from Thomas High School and since the full extent of the issue is currently unknown these scores have been stripped from the data set in order ot adhere to state testing standards.  As such, this analysis was performed twice:  once with all scores and once after the scores in question have been stripped from the data set.

## Resources
* Software:  Python 3.9.7, Anaconda 4.12.0, Jupyter Notebook 6.4.5
* Data sources:  
  * [schools_complete.csv](https://github.com/curt0230/School_District_Analysis/blob/main/Resources/schools_complete.csv)
  * [students_complete.txt](https://github.com/curt0230/School_District_Analysis/blob/main/Resources/students_complete.csv)

## Results
### Impact of data changes
Thomas High School's scores and pass rates were impacted as follows:
* The average math score fell from 83.4% to 83.3%
* The average reading score remained relatively stable at approximately 83.8%
* The percentage of students passing math fell from 93.3% to 93.2%
* The percentage of students passing reading fell from 97.3% to 97.0%
* The percentage of students passing overall fell from 90.9% to 90.3%

At the district level:
  * Overall passing scores dropped .3% from 65.2% to 64.9%
  * Thomas High School maintained its second best ranking based on overall scores

Thomas High School's 9th grade class numbers approximately 460 students out of the 39,170 students in the district, or approximately one percent of the student population.  This sample size is relavent for purposes of statistical analysis.  In general the variance in pass rates after stripping the suspect scores doesn't significantly affect the district-level metrics.

### Overall district performance
PyCity Schools services 39,170 students across 15 schools with an annual budget of approximately $24.6 million.  Across our district, we have a passing rate of approximatley 74.8% of math students and 85.7% of reading students, but our overall passing rate is much lower at 64.9%.

![district_summary.png](/Resources/district_summary.png)


Breaking down the summary above per school, we'll start to see some interesting trends across budgeting, school size, and school type and how they correlate with testing outcomes.

![per_school_summary.png](/Resources/per_school_summary.png)


### Performance by school type
Charter schools do appear to perform significantly better than the district schools across the board.  Math scores are 6 percentage points higher, reading scores are approximately three percentage points higher, and the charter school's overall passing rate is 36% higher than that of the district schools.  The topic of why charter schools perform better than district schools warrants further investigation.

![type_summary.png](/Resources/type_summary.png)


### Performance by school size
Class size is tightly coupled with why it appears our charter schools perform so much better than our public schools.  All schools in the small to medium categories are charter schools, where all the schools in the large category are public schools.  

![size_summary.png](/Resources/size_summary.png)

While this metric is tightly correlated with both scores and pass rates it cannot be taken at face value as the reason charter schools outperform public schools.  There are no samples that cross the groups:  there are no large charter schools and there are no small or medium public schools.  


### Performance by per capita budget
Interestingly enough, per capita spending seems to actually have an inverse relationship with student performance:  as spending increases student performance decreases.  Generally speaking, public schools fall into the higher per capita budget categories.  Larger facilities are required to house larger numbers of students, and often charter schools maintain much smaller athletic programs if they maintain any at all.  This may also end up being justified to an extent, but it is also an area that warrants further investigation.  

![spending_summary.png](/Resources/spending_summary.png)


### School rankings
To illustrate these points, these are the top and bottom 5 ranking schools in the district.  Clearly, there are tightly coupled relationships between budget, class size, and school type when it comes to testing outcomes. 

#### Top 5 schools
![top_5_schools.png](/Resources/top_5_schools.png)


#### Bottom 5 schools
![bottom_5_schools.png](/Resources/bottom_5_schools.png)


## Summary
Based on the data sets used for this analysis it is not possible to identify individual suspect scores or to determine the extent of the impact.  As a result, scores for the full 9th grade class were excluded from analysis to comply with state testing standards.  This did have a minimal impact on the district's reading, math, and overall passing rates as well as those rates for Thomas High School.  The school, however, did maintain its placement as the number two school in the district.  That seems to imply that this issue wasn't terribly pervasive, however the individual student scores should be inspected to identify the offenders.  Once that is achieved this analysis can be repeated on the entire data set, however this may not be deemed necessary given the 99% sample size for the project.
