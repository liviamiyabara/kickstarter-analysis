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
To avoid entering the ranges line by line for this analysis, instead of putting all the ranges into one cell as a text, I split in 3 different cells and put the numbers in a separate the 

### Challenges and Difficulties Encountered

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
![ScreenShot](https://github.com/liviamiyabara/kickstarter-analysis/blob/main/Resources/Theater_Outcomes_vs_Launch.png)

In May and June is when a larger amount of theater campaigns is launched and successful, so we could assume those are the best months to announce a new theater campaign. The number of campaigns decreases as we reach the end of the year, in December we have the lowest amount of campaigns released and the lowest successful rate, therefore Louise should avoid priority campaigns in December. 

- What can you conclude about the Outcomes based on Goals?

- What are some limitations of this dataset?

- What are some other possible tables and/or graphs that we could create?
