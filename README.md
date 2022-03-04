# Fundraising Theatrics: An Analysis of Kickstarter Campaigns

## Objective:

The objective of this analysis was to juxtapose fundraising data about theater pproduction and plays to see what insights there were for a proposed play’s fundraising goal or a campaign launch date for a theater production and relate that to campaigns’ outcomes (success/failure). 

## Process for Theater Campaign Launch vs. Outcome:
In order to analyze the outcomes of theater fundraising campaigns, we utilized a pivot table to describe the amount of successful, failed, and canceled fundraising campaigns in the theater parent category. First, we translated the “Date Launched” variable in the master dataset into a new variable that just described the year the campaign was launched. Then, we filtered the row labels so that analysis was year-agnostic, and the main of time was the month that a given year a campaign’s launch occurred compared to its relative outcome. 

### Challenge: 
* The pivot table did not want to describe campaign results regardless of the year. The pivot table needed to be coerced into giving campaign outcome statistics on a monthly basis, as well as be resorted to better visualize successful outcomes over failed or canceled.

## Process for Play Outcome vs. Campaign Goal:
To analyze outcomes of fundraising for plays vs. their campaign goal, we created bucketed ranges for fundraising goals starting from less $1000, $1000 to $4999, and then moving up in bands of $5000 all the way to fundraising campaigns of more than $50,000. Utilizing excel COUNTIFS() functions, we used the dataset’s variables for campaign outcome and fundraising goal to populate the chart with the number of successful, failed, and cancelled campaigns per each fundraising goal bucket. 

### Challenges:
* A challenge at this stage of the analysis was correctly formatting the syntax of the Excel formulas so as to capture the correct campaign outcome within the correct range of each goal bucket. We then used SUM() to find the total count of plays in each fundraising goal bucket, and then we used that total to calculate the percentage of successful, failed, and cancelled plays per each fundraising goal bucket. 
* A potential challenge across the counting and then calculating the percentages is that there were zero (0) canceled fundraising campaigns for plays. In a dataset of this size, it can be difficult to identify that characteristic by size, and when conducting analysis it can lead to doubting the methodology. But, but reviewing the work done and using other means of testing the analysis (like filtering the original dataset to show any cancelled plays), we can see that the methodology was correct.

## Conclusions about Theater Outcomes by Launch Date:
* May is the launch month with the most successful fundraising campaigns in the theater category, followed closely by June and then July.
* December is the least successful month for campaign launches of theater projects, as the number of successful campaigns is at its lowest and virtually the same as the number of failed (37 compared to 35, respectively).

## Conclusions about Play Outcomes based on Goals.
* The visualized chart shows a spike in successful campaigns as the goal nears and passes the $25000 and $30000 goal buckets, but the sample size for these data points is in the single digits. The percentage calculations from $25000 to $50000 in campaign goal do not properly describe the very small counts of campaigns in the higher-goal buckets. Notable, only 2 out 16 campaigns were successful with fundraising goals in excess of $50,000 or 12.5% success rate and a failure rate of 87.5%.
* In aggregate, campaigns for plays with a fundraising goal that is more modest (less than $15,000) were more likely to be successful than fail.

! [] (https://github.com/bsalamin/kickstarter_analysis_BAS_02242022/blob/main/resources/Goals%20table.png)

## Final Thoughts

### Limitations:
* The dataset is quite outdated. The most recent campaign recorded in the spreadsheet is from May 2017, meaning there could be new trends that are not able to analyzed when it comes to Kickstarter fundraising campaigns and their outcomes. 
* Notably, all of this data is pre-pandemic. The pandemic would probably have had a significant negative effect on campaigns in the theater categories, especially live action productions like plays.
* If the goal is to help Louise raise money for her project generally, this dataset is also limited in that it only covers one single channel she could pursue for fundraising: Kickstarter. There are both other organizations that facilitate crowd-funding that may be better suited for her category, and there also may be organizations uniquely suited to support theater productions.

### Further Analysis:
* It may be useful to look at the other metrics regarding the timing of campaigns and relate them to outcomes. Mapping outcomes against date closed or days-in-the-field (time the fundraiser was live) may give Louise other insights about how to strategize her own campaign.
* Louise may also want to look at average donation and backers count of relevant campaigns with similar categories and goals. Mapping campaigns similar to what she needs for her budget would allow her greater insight into what characteristics a successful campaign should have in terms of goals, backers, average donation, and timing.


