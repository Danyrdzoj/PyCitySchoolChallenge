# PyCitySchoolChallenge
![Image](VBA_Challenge_FirstResults.png?raw=true)
# School_District_Analysis

# Week 4 Challenge

In this challenge, you will use your skills using the Pandas library and Jupyter Notebook. You need to replace incorrect data in columns using logical operations with conditionals; retrieve data from DataFrames; merge, filter, slice, and sort DataFrames; and apply the groupby() function to a DataFrame. Using these methods, you will create a new analysis with the incorrect data removed.

## Background

The grades of the ninth graders at Thomas High School have been changed. While administrators do not know the full extent of this academic dishonesty, they want to uphold the standards of state testing and have turned to you for help.

After assessing the situation with the school superintendent and Maria, you decide the best approach is to:
* Replace the ninth-grade math and reading scores from Thomas High School.
* Keep all other data associated with the ninth-grade students and Thomas High School intact.

## Resources

Pandas & Numpy libraries
Jupyter Notebook (PythonData environment created using Python 3.7 and Anaconda)                      
csv’s provided:  schools_complete.csv, students_complete.csv

## Analysis

The iPython Notebook, PyCitySchools was developed throughout the modules for this week.  Several pandas library dataframes and functions were used to read data from the csv files, build dataframes, and acquire the requested output.  For the challenge, the file was saved as PyCitySchools_Challenge and then the pandas .loc & numpy np.nan functions were used to replace the corrupt student data with “not a number” entries.  Finally, the code was run again with the data replaced and the results are discussed below.

## Conclusions

### How is District Summary affected?
The total schools and total students numbers are unaffected when the Thomas High School 9th grade reading and math scores are removed from the dataset. We continue to report overall averages by district using the same total number of students (39,170). The district's average math score falls from 79.0 to 78.9, but the average reading score remains unchanged (81.9). The overall percentage of students passing math, reading, and both is reduced by 1%. This makes sense given that Thomas High School has 461 ninth-grade students, or about 1.1 percent of the district's total 39,170 students.

#### Fig. 1:  District Summary prior to removing Thomas High School 9th grade scores
![Image](Challenge Im 1?raw=true)

#### Fig. 2:  District Summary after removing Thomas High School 9th grade scores
![Image](Challenge Im 2?raw=true)

### How is School Summary affected?
The School Summary dataframe changes only for Thomas High School because we continue to use the total number of students in each school to calculate the percentage of students who pass math, reading, and both at each school. Obviously, these percentages will fall precipitously for Thomas High School because roughly a quarter of the students will have no score (i.e., a non-passing score), but they will be included in the total students denominator.

### How is Thomas High School’s performance affected when 9th grade scores are removed?
Using the original data set with the corrupted scores, Thomas High School ranks among the top five in the district. Second in the district, in fact, with an overall passing percentage of 90.9. When the erroneous 9th grade results are removed from the dataset, Thomas High School falls out of the Top 5 and into eighth place, with an overall passing percentage of 60.1. This drop of 30% is to be expected given that 461 ninth grade students account for 28% of total students at Thomas High School. There is no way to know the true overall performance of Thomas High School without retesting the 9th grade students.

#### Fig. 3:  Top 5 Schools prior to removing Thomas High School 9th grade scores
![Image](Challenge Im 3?raw=true)

#### Fig. 4:  Top 10 Schools after removing Thomas High School 9th grade scores
![Image](Challenge Im 4?raw=true)

### How does removing scores affect Math & Reading scores by grade?  
As expected, the math and reading scores by grade for all other schools are not affected when the Thomas High School 9th grade scores are removed.  This is due to how the data was grouped into the dataframe.  Nonetheless, there is now a hole in the dataset for these scores.  This can be addressed as discussed above.  

#### Fig. 5:  Math Scores by Grade
#### Before removing Thomas High School 9th grade scores on Left, After on Right 
![Image](Challenge Im 5?raw=true)

#### Fig. 6:  Reading Scores by Grade
#### Before removing Thomas High School 9th grade scores on Left, After on Right 
![Image](Challenge Im 6?raw=true)               

### By School Spending?  
Again, due to how the data was grouped for this dataframe only the bin that contains Thomas High School is affected.  Since Thomas High School’s per student budget is $638, this is the $630-644 bin.  Surprisingly, the average math & reading scores stayed the same.  Yet, because the total number of students includes the 9th grade students with no scores, the percentage of students passing math, reading, and both (overall) has dropped in this bin ~7 points.

#### Fig. 7:  Summary by School Spending prior to removing Thomas High School 9th grade scores
![Image](Challenge Im 7?raw=true)
#### Fig. 8:  Summary by School Spending after removing Thomas High School 9th grade scores
![Image](Challenge Im 8?raw=true)

### By School Size?  
The same can be said for the size of the school.  Thomas High School has 1,635 so it is categorized in the Medium School Size.  Here we see a decrease of ~6 points in the percentage of students passing math, reading, and both (overall).

#### Fig. 9:  Summary by School Size prior to removing Thomas High School 9th grade scores
![Image](Challenge Im 9?raw=true)

#### Fig. 10:  Summary by School Size after removing Thomas High School 9th grade scores
![Image](Challenge Im 10?raw=true)

### By School Type?
Lastly, Thomas High School is a Charter School.  We see a roughly 4 point drop in the percentage of students passing math, reading, and both (overall) without affecting the District Schools. 

#### Fig. 11:  Summary by School Type prior to removing Thomas High School 9th grade scores
![Image](Challenge Im 11?raw=true)
#### Fig. 12:  Summary by School Size after removing Thomas High School 9th grade scores
![Image](Challenge Im12?raw=true)
