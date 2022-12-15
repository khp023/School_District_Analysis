# School District Analysis Project (PyCitySchools)

## Overview of School District Analysis

For a particular school district, students' standardized test data was collected such that we also have each student's grade and school data for analysis.  The database is located in file [new_full_student_data.csv](/Resources/new_full_student_data.csv). Students' performance data is useful for school district's administrative strategy and budgeting decisions; we will be performing analysis by trending and aggregating the data through utilizing the Pandas library on Python. The file [Student_Data_Challenge_Starter_Code.ipynb](Student_Data_Challenge_Starter_Code.ipynb) walks through the data analysis process in which the data is collected, prepared and processed, and analyzed. 

As developed in [PyPoll_Challenge.py](PyPoll_Challenge.py), the success of the analysis will be determined through proper usage of lists, dictionaries, and interative loops to filter the information.

## School District Data Collection and Preparation 

Given the data, in the first deliverable  we initialized [new_full_student_data.csv](/Resources/new_full_student_data.csv) as a Pandas DataFrame to perform analysis. Acknowledging in this case that incomplete or duplicated data is not useful for our analysis, we were able to remove them from our data set through using `student_df.dropna()` and `student_df.drop_duplicates()`, with `student_df` being our dataframe created from [new_full_student_data.csv](/Resources/new_full_student_data.csv)]. It was also ensured that each "column" in the DataFrame was the appropriate data type. 

## School District Data Results 

General statistics of all the numerical data in the dataset were performed through `student_df.describe()`. Using `.loc()` and `.iloc()` methods, we were able to filter the data; for example in retrieving all of the reading scores from Dixon High School, we were able to present the following: 
![Dixon High School](/screenshots/DixonHigh.png)

Aggregating the data using `.groupby()`, we were able to determine each school's total student count: 
![Student Count](/screenshots/Student_count.png)

More importantly, comparisons were performed regarding charter and public schools as follows: 
![School Budget](/screenshots/school_budget.png) ![Math Scores](/screenshots/math_score.png)

## School District Analysis Summary

We can see here an immediate correlation that despite having a lower average school budget, Charter school students perform marginally better in math standardized testing (for grades 9-11). We also see at a glance that there is a large range of school sizes (in regard to number of students), the most in this data set being Montgomery High School at 2038 students and the least being Chang High School at 171 students. It would be useful to further dissect the data to convince ourselves if the lower math scores may be because of a larger sample size- we would need to tabulate how many students are in public schools and how many are in charter schools. Stemming from that, we could also take a look at the distrubution of students in each grade. 