# Kickstarting with Excel

## Overview of Project
Analysis on different campaigns outcome in relation to their launch dates and funding goals. 

### Purpose
To determine if launch dates and funding goals on kickstarter campaigns have a correlation with their outcome.  

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
I created a new column in the kickstart information to obtain the year of each campaign launch date Using the formula =YEAR(S2) and copied down the column. I then created a pivot chart to show theater kickstarter outcomes by month of the year (launch date). This provides a total for each of the three outcome (successful, failed, and canceled) results by month for the parent category of theater. One challenge I faced doing this was determining the correct placement of the pivot chart elements and sorting, By a bit of trial and error, I figured it out fairly quickly. <br>
![Launch Pivot chart](https://user-images.githubusercontent.com/114044192/193434627-2d896be4-e4f0-4567-89fb-22b2082bebf0.PNG)<br>

![Year formula](https://user-images.githubusercontent.com/114044192/193434635-82111e10-d64b-49ae-83d5-56b0e8f0f3dd.PNG)<br>

I then created the graph for Theater Outcomes Based on Launch Date. The biggest challenge on this was trial and error to remove the filter labels. 

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/114044192/193434643-488a285d-591e-4ac4-9638-82cdf9e1b54a.png)<br>

### Analysis of Outcomes Based on Goals
Next was the Outcome Based on Goals using the COUNTIFS function. I did not encounter much difficulty in the initial creation of the new sheet as instructed. However, I again had some trial and error when I started using the formula getting everyting in the correct places with the correct syntax. I copied my formula down the first row and changed the numbers on each line. Again, I used trial and error to get the correct formulas and quickly realized, I needed two conditions for the Goal, I copied the first column to the failed and canceled columns. They all returned zeros. I realized i failed to use the constant indicator ($), so went back and updated the successful row with the constants. =COUNTIFS(Kickstarter!$F:$F,"successful",Kickstarter!$D:$D,"<1000",Kickstarter!$R:$R,"=plays") 

![goal outcome formula](https://user-images.githubusercontent.com/114044192/193434655-991597dc-fde7-450d-84f4-30627a233c57.PNG)<br>

I then added the formula for the percentage successful column remembering to use my constat =B2/$E2. I then copied it down and over successfully. 

Lastly, I created the line graph to show the visual representation of the outcome based on goal and percentage. The first graph I made did not have the lines showing correctly for some reason. I deleted it and created a new one that showed correctly. I edited the data source to only include the Goal an percentage columns. 

![Graph Data Edit](https://user-images.githubusercontent.com/114044192/193434667-879f8089-58ab-449e-be62-757847e72f7d.PNG)<br>

I edited the Axis labels, added title and changed colors.

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/114044192/193434676-13153ce2-0190-4fbb-8930-c240f7113f96.png)<br>

### Challenges and Difficulties Encountered
My first challenge was when I opened my saved Excel file and I was not able to edit anything. I contacted AskBCS and after a lengthy Zoom session, they were not able to figure out why. I thought I was going to have to start over, but discovered it let me move my tabs to a new workbook that allowed me to edit. 

After that, going through the exercises was just trial and error to become familiar with successfully executing pivot charts and graphs as well as using the correct formulas. 

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
1. May is the most successful month for theater kickstart campaigns, closely followed by June and July. After May, the percentage of outcomes for both successful and failed campaigns begin to fall for the remainder of the year with a slight jump in October for both outcomes. 

2. December has the same probabilty of being successful as failing and is the worst month to launch a campaign. 

- What can you conclude about the Outcomes based on Goals?
1. The trends for Percentage successful and percentage failed appear to be almost directly opposite each other based on goal. 

2. The most successful goal amounts are less than $1000 and $35,000 to $45,000. $15,000 to $20,000 are equally likely to succeed and fail. 

- What are some limitations of this dataset?
1. Without the inidividual contributons, we are unable to determine if there are any large donations that may skew the results. 
2. We do not know what events, promotions or oncentives were used in these campaigns that may have affected contributions.

- What are some other possible tables and/or graphs that we could create?
1. The number of days each campaign ran. This would tell us if there is any correlation with outcome and campaign length. 
2. Deadline vs outcome. This would tell us if campaigns ending in certain months were more likely to have a favorable outcome. 
