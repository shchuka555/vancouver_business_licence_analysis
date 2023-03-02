

# vancouver_business_licence_analysis

## Table of Contents

- [Overview](#Overview)  
- [Questions_to_answer](#Questions_to_answer)  
- [Hypothesis](#Hypothesis)  
- [Analysis](#Analysis)

- [Conclusion](#Conclusion)  
- [Credits](#Credits)  




## Overview 
In this project
- Obtained 2 business license datasets from the city of Vancouver and then merged them.
  - The number of rows is roughly 1.6 million, and the columns are 29 after merging.
  - The dataset contains information of business licences in Vancouver from 1996 to 2023.
- Applied my data wrangling skills in python to transform the data into a more analyzable form.
- Analyzed dataset and found trends and seasonality on yearly changes in the number of business licenses issued.
- Hypothesised there is a relationship between economic circumstances and tested it by calculating the correlation between percentage changes in the number of licenses issued each year and measurements of economies. Examples of such measurements are GDP, GNP, and Inflation rate.

## Questions_to_answer
- **Q1 Are there any trends/seasonalities in the time when licences were issued?**
- **21 Are there any trends/seasonalities in the number of issued licences for each license year?**
- **Q3 Are there relationships between changes in number of issued licenses and measurements of economy? **




## Analysis


## part1 Plotting number of licences issued everyday vs different time spans.

#### In this part, I will take a narrow down approach 

## Figure1 to 5: Daily counts of issued licences. 

### 1
![https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/total_count.png](https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/total_count.png)
- As you can see, there is a seasonality in the plot. It looks like many Bus-license were issued between the end and the beginning of the year. However, it is hard to see the seasonality due to the long time length. 
- So, let's narrow down the x-axis from 2016 to 2019!!
### 2
![https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/2015-2018_year.png](https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/2015-2018_year.png)
- The plot clearly shows seasonality in the daily number of issued licences. 
- Looks like the curve is centred around every January, and there is another curve after January as well, but not clear when.
- Let's plot a bar chart to see which months have the highest count.

### 3
![https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/month_count.png](https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/month_count.png)
- The plot tells most business obtain new licenses between November to February and December has a highest count.
- The duration is long probably due to the fact that workers who issue licences have own capacity to hundle all applications.  
- Just like how it takes more than few month to receive Study Permit or Work Permit in Canada.
### 4
![https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/2016-2017.png](https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/2016-2017.png)
- This is narrowed version of plot two, and the period is from November 2016 to March 2017.
- It shows three recognizable patterns, which are stationary, downward trends and upward trend.
-  There is stationarity between November and December 2016 because it has a steady moving average and the variance seems fixed. 
- However, the plot shows downward trends after the Christmas season because the moving average keeps dropping till the beginning of February.
- Subtle upward trend was observed in February because there was a slight increase in the moving average over a few weeks, but it got lower again from the beginning of March 2017.
- One interesting thing is that there are constant fluctuations every week; it might be due to the weekly schedule of workers who process the applications.
- Let's narrow down again to determine the factor of fluctuations.
### 5
![https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/2016_nov.png](https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/2016_nov.png)
- According to the [year 2016 calendar](https://www.timeanddate.com/calendar/?year=2016&country=27), the days which have significantly low number of issued licences are weekends or holidays.
- It seems plausible to think the number of applications issued drops during weekend and holidays because most workers do not work on these days.
-  Yet, still surprising to see some workers still process the business licenses applications on holidays.

## Figure5: Hourly counts.

![https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/hour_count.png](https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/hour_count.png)
![https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/hour_detail_count.png](https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/hour_detail_count.png)

### First plot.
- This first plot shows licences were issued during the standard working hours (8am~6pm).
- Assuming the following things
  - Productivity of officers is highly correlated with the number of licences/permissions they issue.
  - Workers work between 8am to 6pm and take a lunch break between 12 to 1pm. 
 - The plot seems consistent with the productivity of standard office workers because the number increases throughout noon. The peak is between 10 am and 12 pm, but the number decreases during lunch break. After the break, the number of applications issued increased from 1~3pm but kept falling again after 3 pm till the end of work time.
- If the above two assumptions are valid, then it is possible to think officers of business licences work normally.

### Second plot.
- Splitted the countings into each of those most actively issued months. 
- It shows hourly changes in workers productivity are consistent regardelss of months.

## Figure6: Percentage changes in number of licenses for each license holding year.
![https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/folderyear_line_.png](https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/folderyear_line_.png)
![https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/pct_change_year_bar.png](https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/pct_change_year_bar.png)

### First plot.
- This plot shows an upward trend in total number of business licenses issued in each years.
- Also there are some fluctuations. For example, it significantly droped in 2020 and presumably due to the pamdemic of covid-19. 
- Despite there are some big drops in 2020, the number got recovered in 2022. 
- The question is **"Are these values correlated with changes in Canadian economy?"**

### Second plot.
- This plot shows same data as previous plot but in bar chart and shows percentage changes in number of licenses compared with preivious year.
- It shows there are tiny decrease in number of licences in 2008 comapred with 2007, which should be much bigger drops if the economy is positively correlated with the number of each year's business licenses.

## Part2 Testing Hypothesis: Is there correlation between changes in number of licenses and mesurements of ecnomy ?

There is almost no linear relationship between changes in number of issued business licenses with changes in GDP and Inflation rate.
However,GNP showed weak Pearson's correlation.
Therefore, I will investigate the variable.


Plot1: Standardized changes in GNP vs Business license issued number. 

![https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/gnp_vs_bl2.png
](https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/gnp_vs_bl2.png
)
- Assuming business owners respond to GNP changes in the same year.
- Both shows negative changes in 2020 and strong resilience in 2021.
- Other than after the pandemic, it seems like both line charts fit well if business owners respond previous year's GNP.

Plot2: Standardized changes in GNP vs Business license issued number part 2.
![https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/shifted_gnp_vs_bl2.png
](https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/shifted_gnp_vs_bl2.png
)
- Assuming business owners respond to GNP changes in the previous year.
- Both line charts fit very well between 2000 to 2005, 2010 to 2018.
- However, the charts do not fit after 2019.

### Summary 
- It seems plausible to assume business owners responded to the previous year's domestic economy when it is stable. Stable means neither rapid growth nor strong recession.
- Also plausible to assume business owners started responding to the same year's domestic economy since 2020. 
- Although changes in GNP does not fit perfectly well with changes in number of business license issued, GNP growth rate can be use as a approximate predictor in  business license issues for next year.


## Conclusion
- The number of business licenses is kept increasing in recent 25 years.
- Pandemic affected negatively but showed strong resilience after 2020.
- Most owners receive their licenses between November and February.
- Business owners presumably responded previous year's domestic economy the past but started to respond to the current year's domestic economy after the pandemic.


## Credits

Dataset from 
- [City of Vancouver Business licences: 1997-2012](https://opendata.vancouver.ca/explore/dataset/business-licences-1997-to-2012/export/?disjunctive.status&disjunctive.businesssubtype)
- [City of Vancouver Business licences: 2013-2023](https://opendata.vancouver.ca/explore/dataset/business-licences/information/?disjunctive.status&disjunctive.businesssubtype)
- [Canadian Economics data](https://www.macrotrends.net/countries/CAN/canada/inflation-rate-cpi)


Used informatations from [Statistics Canada](https://www150.statcan.gc.ca/t1/tbl1/en/tv.action?pid=3310027001&pickMembers%5B0%5D=1.42&pickMembers%5B1%5D=2.1&cubeTimeFrame.startMonth=05&cubeTimeFrame.startYear=2022&cubeTimeFrame.endMonth=09&cubeTimeFrame.endYear=2022&referencePeriods=20220501%2C20220901)

