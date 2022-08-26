# Kickstarting with Excel

## Overview of Project

### Purpose: 
This project aims to analyze data from different campaigns and to know how they performed in relation to their launch dates and funding goals.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date:
For this analysis it was necessary to work first on the Kickstarter tab.
> To convert to date the column "launched_at" and create the column "Date Created Conversion" we used the formula (((J2/60)/60)/24)+DATE(1970,1,1)
For the separation of the "Category and subcategory" column in 2 and facilitate the use of Category as a filter we use the Text to Columns command using '/' as delimiter and created the columns "Category" and "Subcategory".
To obtain the results of the Theaters based on the launch dates, we created a Pivot Table in a new worksheet labeled "Theater Outcomes by Launch Date" with the following parameters:
Filters: 
- "Parent Category" and "Years"
- "Parent Category" was filtered on "theater"
Columns: 
- "Outcomes"
Rows: 
- "Date Created Conversion" (only months of the year displayed)
Values: 
- "Count of Outcomes"
Campaign outcomes were sorted in descending order.
The line chart titled Theater_Outcomes_vs_Launch was created com base na Pivot Table and showing the number of successful, failed, or canceled projects by month as the image shown below.
![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/111664141/186991356-bb832d1b-b9ca-49a9-9850-796db44289a5.png)


### Analysis of Outcomes Based on Goals
For this analysis, we created a new worksheet and labeled it "Goal-Based Results".
In the new worksheet, I created the following columns:
Goal, Number Successful , Number Failed , Number Canceled , Total Projects, Percentage Successful , Percentage Failed , Percentage Canceled 
In the "Goal" column, we create dollar value ranges to group projects based on the target value.
To determine each value by results for the subcategory “plays” we use the 'Counts' function.
To calculate the total per result for each range we use the 'SUM' function.
For the percentage, we just divide the value of each range by the total of its respective result and format it as "percentage".
Finally, we created the line chart titled "Outcomes Based on Goal" to visualize the relationship between the goal-amount ranges and the percentage of successful, failed, or canceled projects, which can be viewed below.
![Outcomes_vs_Goals](https://user-images.githubusercontent.com/111664141/186991436-efb1ce58-81ea-4aac-a708-8b2a58ab1468.png)


### Challenges and Difficulties Encountered
The challenges encountered were mainly the columns where it was necessary to convert data because it was not feasible to use them in the formats in which they were made available. It was also necessary to validate the case totals between the pivot table and the main table, since the range of values was diverse and very susceptible to data loss if the functions were incorrect.

## Results

### Conclusions about the Outcomes based on Launch Date:
The first analysis that we can make in the "Outcomes based on Launch Date" is that, regardless of the month of release, the theater campaigns had more successful results than failed or canceled, with only the month of December being the only exception. 
It is also possible to see that the months of May, June and July, successively, are the months where the campaigns had the best results.

### Conclusions about the Outcomes based on Goals:
In the Outcomes based on Goals analysis of the plays we can see that the higher the value of the campaign, the greater the chances of being unsuccessful. 
Based on the analysis of the chart with the same name above, for campaigns up to a value of $15000 the results were positive and from this value onwards the results began to decline, leaving only the range from S35000 to $4500 with good results. 
We can also verify that no play has been cancelled.

### Limitations of this dataset and sugestions:
Latest launch date is from 2017 which may not reflect current day. 
For the case study of theaters, it would be interesting to have the data of the writers/actors as it would help to analyze the probability of the campaigns being successful.
As sugestion, we could create tables analyzing the outcomes of launch dates by country and the average time of campaigns in relation to outcomes.



