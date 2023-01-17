# Pandas-Challenge
The pandas challenge for module 4 of the Georgia Tech bootcamp


Instructions


Using Pandas and Jupyter Notebook, create a report that includes the following data. Your report must include a written description of at least two observable trends based on the data.

Hint: Check out the sample solution called PyCitySchools_starter.ipynb located in the .zip file to review the desired format for this assignment.

District Summary
Perform the necessary calculations and then create a high-level snapshot of the district's key metrics in a DataFrame.

Include the following:

Total number of unique schools

Total students

Total budget

Average math score

Average reading score

% passing math (the percentage of students who passed math)

% passing reading (the percentage of students who passed reading)

% overall passing (the percentage of students who passed math AND reading)

School Summary
Perform the necessary calculations and then create a DataFrame that summarizes key metrics about each school.

Include the following:

School name

School type

Total students

Total school budget

Per student budget

Average math score

Average reading score

% passing math (the percentage of students who passed math)

% passing reading (the percentage of students who passed reading)

% overall passing (the percentage of students who passed math AND reading)

Highest-Performing Schools (by % Overall Passing)
Sort the schools by % Overall Passing in descending order and display the top 5 rows.

Save the results in a DataFrame called "top_schools".

Lowest-Performing Schools (by % Overall Passing)
Sort the schools by % Overall Passing in ascending order and display the top 5 rows.

Save the results in a DataFrame called "bottom_schools".

Math Scores by Grade
Perform the necessary calculations to create a DataFrame that lists the average math score for students of each grade level (9th, 10th, 11th, 12th) at each school.

Reading Scores by Grade
Create a DataFrame that lists the average reading score for students of each grade level (9th, 10th, 11th, 12th) at each school.

Scores by School Spending
Create a table that breaks down school performance based on average spending ranges (per student).

Use the code provided below to create four bins with reasonable cutoff values to group school spending.

spending_bins = [0, 585, 630, 645, 680]
labels = ["<$585", "$585-630", "$630-645", "$645-680"]
Use pd.cut to categorize spending based on the bins.

Use the following code to then calculate mean scores per spending range.

spending_math_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"]).mean()["Average Math Score"]
spending_reading_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"]).mean()["Average Reading Score"]
spending_passing_math = school_spending_df.groupby(["Spending Ranges (Per Student)"]).mean()["% Passing Math"]
spending_passing_reading = school_spending_df.groupby(["Spending Ranges (Per Student)"]).mean()["% Passing Reading"]
overall_passing_spending = school_spending_df.groupby(["Spending Ranges (Per Student)"]).mean()["% Overall Passing"]
Use the scores above to create a DataFrame called spending_summary.

Include the following metrics in the table:

Average math score

Average reading score

% passing math (the percentage of students who passed math)

% passing reading (the percentage of students who passed reading)

% overall passing (the percentage of students who passed math AND reading)

Scores by School Size
Use the following code to bin the per_school_summary.

size_bins = [0, 1000, 2000, 5000]
labels = ["Small (<1000)", "Medium (1000-2000)", "Large (2000-5000)"]
Use pd.cut on the "Total Students" column of the per_school_summary DataFrame.

Create a DataFrame called size_summary that breaks down school performance based on school size (small, medium, or large).

Scores by School Type
Use the per_school_summary DataFrame from the previous step to create a new DataFrame called type_summary.

This new DataFrame should show school performance based on the "School Type".

Requirements
District Summary (20 points)
Calculate the total number of unique schools (2 points)
Calculate the total number of students (2 points)
Calculate the total budget (2 points)
Calculate the average (mean) math score (2 points)
Calculate the average (mean) reading score (2 points)
Use the code provided to calculate the percentage of students who passed math (2 points)
Calculate the percentage of students who passed reading (2 points)
Use the code provided to calculate the percentage of students that passed both math and reading (2 points)
Create a new DataFrame for the above calculations called district_summary (4 points)
School Summary (20 points)
Use the code provided to select the school type (2 points)
Calculate the total student count (2 points)
Use the code provided to calculate the per capita spending (2 points)
Calculate the average test scores (2 points)
Calculate the number of schools with math scores of 70 or higher (2 points)
Calculate the number of schools with reading scores of 70 or higher (2 points)
Use the provided code to calculate the schools that passed both math and reading with scores of 70 or higher (2 points)
Use the provided code to calculate the passing rates (2 points)
Create a new DataFrame for the above calculations called per_school_summary (4 points)
Highest-Performing Schools by Percentage of Overall Passing (5 points)
Sort the schools by % Overall Passing in descending order (2 points)
Save the results to a DataFrame called top_schools (2 points)
Display the first 5 rows (1 point)
Lowest-Performing Schools by Percentage of Overall Passing (5 points)
Sort the schools by % Overall Passing in ascending order (2 points)
Save the results to a DataFrame called bottom_schools (2 points)
Display the first 5 rows (1 point)
Math Scores by Grade (10 points)
Use the code provided to separate the data by grade (1 points)
Group by "school_name" and take the mean of each (4 points)
Use the code to select only the math_score (1 points)
Combine each of the scores above into single DataFrame called math_scores_by_grade (4 points)
Reading Scores by Grade (10 points)
Use the code provided to separate the data by grade (1 points)
Group by "school_name" and take the mean of each (4 points)
Use the code to select only the reading_score (1 points)
Combine each of the scores above into single DataFrame called reading_scores_by_grade (4 points)
Scores by School Spending (5 points)
Use pd.cut with the provided code to bin the data by the spending ranges (2 points)
Use the code provided to calculate the averages (1 points)
Create the spending_summary DataFrame using the binned and averaged spending data (2 points)
Scores by School Size (5 points)
Use pd.cut with the provided code to bin the data by the school sizes (2 points)
Use the code provided to calculate the averages (1 points)
Create the size_summary DataFrame using the binned and averaged size data (2 points)
Scores by School Type (5 points)
Group the per_school_summary DataFrame by "School Type" and average the results (2 points)
Use the code provided to select the new column data (1 point)
Create a new DataFrame called type_summary that uses the new column data (2 points)
Written Report (15 points)
To receive all points, the written report presents a cohesive written analysis that:

Summarizes the analysis (5 points)

Draws two correct conclusions or comparisons from the calculations (10 points)


_________________________________________________________________________________________________________________________________

The analysis

The start of the program is first devoted to the importing of the csv files found in the Resources folder.

This is then followed up with the merging of the two data sets to one dataframe.

It is then broken up into different segments
    District Summary
    School Summary
    Highest-Preforming Schools (by % Overall Passing)
    Bottom Performing Schools (By % Overall Passing)
    Math Scores by Grade
    Reading Score by Grade
    Scores by School Spending
    Scores by School Size
    Scores by School Type



A Few Observation, Conclusions, and Comparisons

1)The Charter schools appears to be beating District schools in every catagory.
    The biggest difference being in the % passing in Math, Reading, and especially in the % overall passing.
    
2)The size of the school really matters between the jump between Medium (1000-2000) and Large (2000-5000).
    The relationship is in a negative correlation with larger schools falling the most behind.
    There is not much difference betweeen small (<1000) and Medium schools.
    
Note: Most Charter schools are small to Medium schools.

3)Spending per student varies but shows a trend that less money actually yields more results
    Average Reading has the least gains in this trend with less than 2% difference.
    The biggest gains are in % Overall Passing.
    Per student spending has a bigger effect on % Passing over Averages.

4) You do not see much change in averages in both math and reading across different grade levels when it comes to the indiviual schools.


Conclusion: Smaller schools (usually charter schools) preform better then larger highly funded schools.


