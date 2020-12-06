# kickstarter-analysis
Challenge 1
# Kickstarting with Excel

## Overview of Project

### Purpose
In the spreadsheet we have the data of Louise’s fundraising campaigns and we will make an analysis to understand how different the Theater campaigns performed in relation to their launch dates and their funding goals.
## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
To be able to read the launched date, I converted the Unix timestamps, which measure time as the number of seconds since midnight of January 1, 1970 to the standard date format of month/day/year by using the formula =((( cell with unix timestamp /60)/60)/24)+DATE(1970,1,1). Once that step is done, it was easy to create a pivot chart with the filter of the ‘Parent category’ for ‘theater’, in the rows the ‘Date for created conversion’, on the columns the ‘outcomes’ and for the values the ‘Count of id’.
### Analysis of Outcomes Based on Goals
To avoid entering the ranges in the formula line by line for this analysis, instead of using only column A to show all tiers in one cell, I split into 3 columns to make it easier to refer a formula to a specific number. 
Then for the COUNTIFS formula, in the goal range criteria I’ve used the quotes “” to determine the formula with the ranges: less than (“<”), between (“>=” and “<=”), greater than (“>”). Then I added the “&” to refer to the numbers of those ranges in column A and C, and then I was able to copy the formula from row 3 to row 12:
![ScreenShot](https://github.com/liviamiyabara/kickstarter-analysis/blob/main/Screenshots/Screenshot_analysis.png)

For the 'Number failed’ and ‘Number cancelled’, I copied the same formulas for the ‘Number Successful’ and used the CTRL+H shortcut for the replacement, I changed ‘successful’ for ‘failed’ and ‘canceled’ for the selected rows to  update the right conditions to the formula. 
Then the last steps were easier, just using the sum formula and dividing the cells to get to the percentage.

### Challenges and Difficulties Encountered
The biggest challenge was to combine the logic of the ranges (less than, between, greater than) with cells to automate the analysis of the ‘Outcomes Based on Goals’, it would be time consuming if I’ve had to write a specific formula to each row of the Number of successful campaigns. This was accomplished by combining quote sign for less than (“<”), between (“>=” and “<=”), greater than (“>”) with the “&” to refer back to a cell. 
## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
![ScreenShot](https://github.com/liviamiyabara/kickstarter-analysis/blob/main/Resources/Theater_Outcomes_vs_Launch.png)

In May and June is when a larger amount of theater campaigns is launched and successful, so we could assume those are the best months to announce a new theater campaign. The number of campaigns decreases as we reach the end of the year, in December we have the lowest amount of campaigns released and the lowest successful rate, therefore Louise should avoid priority campaigns in December. 

- What can you conclude about the Outcomes based on Goals?
![ScreenShot](https://github.com/liviamiyabara/kickstarter-analysis/blob/main/Resources/Outcomes_vs_Goals.png)
The percentage of successful campaigns is higher for the lowest 2 tiers (less than 1000 and 1000 to 4999), so campaigns with the goal lower than 5000 have a higher probability to succeed. The campaigns with the high goal ranges of 35000 to 39999 and 40000 to 44999 have a better success rate than the ones between 5000 to 34999, which can indicate other influencing factors besides the goal amount of a campaign.
- What are some limitations of this dataset?
If the goal of the analysis is to understand how to create more successful campaigns, one limiting factor could be that the dataset is not including all the relevant criteria that determine that. It would be good to understand from the donators what are the criteria that influence their decision (i.e. the method of communication: magazine, website, mail, social media) and include those factors in the study.
- What are some other possible tables and/or graphs that we could create?
One suggestion would be to change the chart type for the 'Outcome Based on Goals' to the '100% Stacked Column', this will simplify how the user can see the data:
![ScreenShot](https://github.com/liviamiyabara/kickstarter-analysis/blob/main/Screenshots/Chart%20suggestion.png)
