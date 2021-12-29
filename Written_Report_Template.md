# Kickstarting with Excel

## Overview of Project

### Purpose
This analysis was intended to help Louise begin and plan her crowdfunding campaign to help fund her play Fever by determining specific factors or trends that make a project’s campaign successful. Specifically, this analysis helps visualize campaign outcomes based on their launch dates and funding goals. This will provide Louise with information on how launch dates and funding goals may be influencing the success of crowdfunding campaigns so that she can set her own campaign accordingly. 


## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/94864663/147695684-be294e44-1339-4bd7-b53c-cdcfb16ac7be.png)
Figure 1. Number of theater campaigns that were successful, failed, or canceled from each month across multiple years. 


Below is the pivot table generated from the original Kickstarter dataset. The table shows the number of campaigns for each outcome based on the month they were launched with the option of filtering for parent category and years. In this case the table does not filter for a specific year but filters for theater campaigns.

![Launch_Date_Pivot](https://user-images.githubusercontent.com/94864663/147699235-f50fa788-b1fc-4fa1-aef2-de931d0fc1b6.png)


Below are the pivot table fields for reference:

![Pivot_Fields](https://user-images.githubusercontent.com/94864663/147699289-09f3c683-fa3b-4a98-8642-9969e2966e65.png)


### Analysis of Outcomes Based on Goals

![Outcome_vs_Goals](https://user-images.githubusercontent.com/94864663/147695691-0cb38b06-6b02-4deb-9e29-c1500b749dd6.png)
Figure 2. Percentage of successful, failed, and canceled campaigns based on their fundraising goals.


A COUNTIFS formula was used to count the number of plays based on each outcome and goal. Therefore, the formula needed to count the number of campaigns in each goal range by looking at column D and filter for plays in column R while also filtering for each specific outcome in column F from the original dataset. An example formula is provided below. This formula is counting the number of successful campaigns for plays with goals between $1000 and $4999.

![Based_on_Goals_Formula](https://user-images.githubusercontent.com/94864663/147698896-a7724a1d-1a74-4246-94f7-a9bf21d29842.png)

To calculate a percentage, the rows needed from each column outcome needed to be summed. Therefore, total outcomes equal the sum of successful, failed, and canceled projects in each row. The formula “= SUM (B2:D2)” was used to determine these totals. Then the percentages were found by dividing the number of projects for each outcome by their total for each row. For example, the number of successful campaigns for plays with goals less than $1000 was 141, and the total number of projects with goals less than $1000 was 186. Therefore 141/186 (75.1%) of campaigns for plays with goals less than $1000 were able to succeed. 

Below is the table of values for reference:

![Goals_Table](https://user-images.githubusercontent.com/94864663/147699026-a43994cc-c187-47cd-9ad9-6274ebc20e53.png)

### Challenges and Difficulties Encountered

In the analysis, I spent a little extra time with the COUNTIFS formula because I realized the trends in chart and pivot table did not make sense conceptually with the numbers in the dataset. I found the trends on the chart also did not match with the chart on the challenge instructions, so I decided to check my formula on excel. After some troubleshooting, I found that I had specified the formula to check numerical values in the “pledged” column (Column E) rather than the goals column (Column D). I believe I encountered this challenge because I typed in these column values rather than moving from sheet to sheet and selecting the columns when writing the formula.  Ultimately, it was a quick fix, and I found the chart matched the overall data appropriately after I made the changes. 


## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

1. Most campaigns for theater were successful between April and August. The month with the highest amount of successful theater campaigns was May with 111 successful campaigns. 

2. July and October were the months with the greatest number of failed theater campaigns with 50 failed campaigns during each month. 

- What can you conclude about the Outcomes based on Goals?

Most campaigns with goals of $45,000 and over tend to fail, and nearly 76% of campaigns with goals under $1000 succeed. Based on the data, it is best to have goals that are anywhere between less than $1000 and $15000. Whereas only 50% of campaigns with goals between $15,000 and $19,000 succeed. In this dataset, 100% of the campaigns with goals between $45,000 and $49,999 failed; only 12.50% of campaigns succeeding with goals greater than $50,000. However, roughly 67% of campaigns with goals between $35,000 and $44,999 were able to succeed. 

- What are some limitations of this dataset?

One limitation the dataset may have been that the data collected is very broad in that values span across many years and countries. Therefore, while the data may show trends, they may not be an extremely accurate representation of the conditions Louise may encounter when she sets up her own campaign. For example, the level of interest for theater may change depending on a specific year or country. These limitations can be accounted for by filtering by more recent years and the country which Louise is from. Extreme values may also skew trends in the dataset, which is why it is also important to be wary of outliers. 


- What are some other possible tables and/or graphs that we could create?

For factors specific to Louise, a table/graph specifying recent years and the country where Louise lives in will help narrow down trends that may contribute to the success of her campaign. It may be beneficial to Louise to examine how successful theater campaigns have been over the years. Showing the percentage successful, failed, and canceled by each year for theater campaigns as a line chart may provide insight on which years produced the most successful campaigns. It may also be interesting to look at differences in average donations based on goals for theater campaigns. This can be accomplished by setting ranges for average donations and plotting against ranges of goals. 
