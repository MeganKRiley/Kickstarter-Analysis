# Kickstarting with Excel

## Overview of Project

### This project is analyzing how different campaigns fared in relation to their launch dates and their fundraising goals

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
    I began my analysis of outcomes based on launch date by adding an additional column to the Kickstarter worksheet and using the `YEAR()` formula to populate the year the campaign launched. With this new column created, I inserted a pivot table that showed a count of canceled, failed, and successful theater campaigns, corresponding with which month they launched.  After transforming this data into a pivot chart, it was easy to visually see that the months in spring and early summer were when the most successful campaigns launched.

   ``` =YEAR(S2) ```

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/90050622/134812137-34bff832-a5f3-40b1-a392-a89e6b908453.png)

### Analysis of Outcomes Based on Goals
    The analysis of outcomes based on goals started with the creation of an additional worksheet, where `COUNTIFS()` formulas were used to calculate the total amount of successful, failed, and canceled campaigns for plays that fell within twelve specified monetary goal ranges.  I then used `SUM()` forumlas to calculate the total counts of projects in each goal range, in order to easily calculate what percentage of the campaigns for each goal were successful, canceled, or failed.  

   ``` =COUNTIFS(Kickstarter!F:F,"Successful",Kickstarter!D:D,"<1000",Kickstarter!R:R,"plays") ```
   ``` =SUM(B2:D2) ```
   ``` =B2/E2 ```

![Outcomes Based on Goal](https://user-images.githubusercontent.com/90050622/134812109-effd777c-7b2f-40c2-8c13-0bfdf8eeff6e.png)

### Challenges and Difficulties Encountered
    I did not run into many issues on the analysis of outcomes based on launch date, but I think it would be easy to forget to remove the outcome for live campaigns from the pivot table, which would then give you an extra line on the line chart. I did initially struggle with the `COUNTIFS()` function on the analysis of outcomes based on goals section.  While I found the initial function looking for goals less than 1000 to be pretty straight forward, I struggled with accuracy as the formulas got significantly longer for the goal ranges that required an additional criteria added.  To keep things simple for myself I excluded the $ before the column letter, which made the formula a lot easier to read and verify, but did require that I enter in the formula more times, as I could not copy and paste as easily.  As I get more experienced in my function writing, I will aim for more efficient solutions to the problems I come accross. 

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
  * The first thing I noticed when reviewing the pivot table and chart for Theater Outcomes Based on Launch date was actually the consistency of the canceled campaigns from month to month. While the overall amount of canceled campaigns is small, it is very evenly spread across each month. In regards to the launch date of canceled campaigns, the highest number is in January, which I would assume coorelates with the beginning of the calendar year, however our data also shows us that successful campaigns rarely launch around the winter holidays, which could be an indicator of why those campaigns inevitably were canceled.  An easy conclusion to pull from this data analysis is that most successful campaigns launch in May.  In fact, the four most launched months for successful campaigns are all months that fall in a row.  They are May, June, July, and then August.  I would encourage Louise to launch her campaign in early summer as well, and to avoid the winter holidays if possible. 

- What can you conclude about the Outcomes based on Goals?
  * There are quite a few things that the outcomes based on goals analysis can tell us.  While the smallest monetary goals tend to have the highest success rate, specifically if under 5,000 dollars, the success rate does not continue to go down all the way to the highest goal grouping.  The success rate does go down all the way to the range of 25,000 to 29,999, after that it actually goes back up, very dramatically, through 35,000 and 44,999.  At 45,000, however, we see an even more dramatic drop in success rate.  It's no surprise that small goals tend to be easy to reach, but if I had to guess why the success rate jumps back up at 30,000 I would make two assumptions.  The first, being that with a higher goal the demand for careful and thoughtful planning was much more of a necessity, and the second, being that with required monetary goals that high, the projects are probably much larger and public interest is probably significantly higher, leading to more donations.  

- What are some limitations of this dataset?
  * The biggest limitation to this dataset is room for human error in regards to execution of these campaigns. We can see data on how each campaign did, but we can't see data on how well prepared each organizer was to tackle such large fundraisers.  It is very possible that certain campaigns failed, not because of their launch date or goal, but because the organizer was not implementing a smart, well thought out campaign.  A similar statement could be made about successful campaigns.  Their success may have been primarily due to the organizers themselves, however, within this dataset we have no way of knowing that. 

- What are some other possible tables and/or graphs that we could create?
  * I would be very interested in seeing some visuals on how long successful, failed, and canceled campaigns ran for.  I think that run time would supplement our data on launch dates very well, and give us critical information to share with Louise on how to have the most successful campaign possible.  I think it could also be very useful information for Louise to know the average amount of backers successful campaigns with similar goals to hers had, as well as what the average donation per backer was.  This would help significantly in her planning and give her a great glimpse into what it is going to take to reach her goals.  
