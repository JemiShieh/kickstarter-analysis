# An Analysis of Kickstarter Campaigns

## Overview of Project

Organize, format, filter, sort, analyze, and visualize Kickstarter campaign data on behalf of up-and-coming playwright Louise to help crowdfund her new play *Fever*

### Purpose

Determine any specific factors that contribute to a project's success in order to help Louise plan a successful Kickstarter funding campaign for *Fever*   

## Analysis and Challenges

Specific data analysis and visualization performed to determine Theater Outcomes Based on Launch Date and Outcomes Based on Goals

[Kickstarter_Challenge.xlsx](https://github.com/JemiShieh/kickstarter-analysis/files/7362339/Kickstarter_Challenge.xlsx)

### Analysis and Visualization of Theater Outcomes Based on Launch Date

* Created "Years" column based on the "Date Created Conversion" column

* Created pivot table in new worksheet labeled "Theater Outcomes by Launch Date"

* Filtered pivot table by "Parent Category" and "Years"

* Filtered "Parent Category" by "theater"

* Changed row labels to display the months of the year 

* Sorted campaign outcomes in descending order

* Created line chart showing the number of "successful," "failed," and "canceled" projects by month

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/92612370/137680988-68810aed-5a0b-491a-b01e-71e3d6e8eb0b.png)

### Analysis and Visualization of Outcomes Based on Goals

* Created new sheet to calculate the Number and Percentage of "successful," "failed," and "canceled" projects by a range of fundraising "goals"
    
  * Used COUNTIFS() function to populate the "Number Successful," "Number Failed," and "Number Canceled" columns, based on the project "outcome," the "goal" amount using the stipulated goal ranges, and the "subcategory" "plays"
    
  * Used SUM() function on each row to add the "Number Successful," "Number Failed," and "Number Canceled" columns to populate the "Total Projects" column
    
  * Calculated percentage of "successful," "failed," and "canceled" projects based on the data from the "Total Projects," "Number Successful," "Number Failed," and "Number Canceled" columns
    
* Created line chart with the goal-amount ranges on the x-axis, and the percentage of "successful," "failed," or "canceled" projects on the y-axis

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/92612370/137681059-e240ec84-cbe6-493a-a8e9-59fc82c7286c.png)

### Challenges and Difficulties Encountered

* Dates required conversion from Unix timestamps to readable format

* Creating "Parent Category" and "Subcategory" columns required splitting text to columns

* Data required filtering to determine subset of comparable projects for "theater" and "plays"

* Manually nested COUNTIFS() are not as efficient as potentially using tables with VLOOKUP() or VBA macros

## Results

* What are two conclusions you can draw about the Theater Outcomes based on Launch Date?

  1. There is a spike of successful campaigns that begin in June, but tapers off by December.
 
  2. There are more successful (61%) campaigns than failed (36%) and canceled (3%) campaigns combined in every month of the year except December, which is also the month with the lowest number of campaigns launched.

* What can you conclude about the Outcomes based on Goals?

  1. Campaigns with the lowest fundraising goals (<$5,000) are far more successful than those with the highest fundraising goals (>$45,000), which also have the highest rate of failure. 

* What are some limitations of this dataset?

  1. Some potential limitations of this dataset include formatting, completeness, accuracy, adequacy, and qualitative measures and context contributing to each specific outcome.   
* What are some other possible tables and/or graphs that we could create?

  1. To help Louise identify additional specific factors that contribute to a project's success, further data analysis and visualization could be conducted to determine the optimal Number of Backers and Average Donation for comparable projects, as well any potential correlations between Kickstarter Staff Pick and Spotlight campaigns and Outcomes.  
