

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


- Bonus section, plotted number of fianancial institutions located in each Vancouver distrcits.
 
## Questions_to_answer
- **Q1 Are there any trends/seasonalities in the time when licences were issued?**
- **21 Are there any trends/seasonalities in the number of issued licences for each license year?**
- **Q3 Are there relationships between number of licences for each license years **

## Hypothesis
- **1 Self-development books are one of the top-seller genres.**
- **2 Bestseller books tend to have higher ratings.**
- **3 Rating is a big purchasing factor for customers nowadays because many people check reviews before buying goods and services. For example, restaurants, online shopping and Airbnb.**
  



## Analysis




## part1 plotting changes in year,month, hours etc.

#### Figure1: Number of issued licences from 1997 to 2022
![https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/total_count.png](https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/total_count.png)
- As you can see, there is a seasonality in the plot. It looks like many Bus-license were issued between the end and the beginning of the year. However, it is hard to see due to long time length. Let's plot yearly and monthly counts !!

#### Figure2: Yearly counts.
![https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/year_count.png](https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/year_count.png)
- The plot shows there is an upward trend on number of lincences issued in Vancouver.
- Also there are some fluctuations. For example, it significantly droped in 2020 and presumably due to the pamdemic of covid-19. 
- Each year in the plot means the time when the licenses were issued. It's not always same the licence year. For example, some businesses apply for 2023 licenses on 2022 and receive it on 2022 December.


#### Figure3: Monthly counts.
![https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/month_count.png](https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/month_count.png)

- The plot shows better undersanding of Figure1 because it captures the seasonality which captured in first plot very well. In total, most business obtain new licenses between November to February. The duration is long probably due to the fact that workers who issue licences have own capacity to hundle 
all applications.  Just like how it takes more than few month to receive Study Permit or Work Permit in Canada.


#### Figure4: Hourly counts.
![https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/hour_count.png](https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/hour_count.png)
- This plot shows licences/permissions were issued during standard working hour (8am~6pm).
-Assuming following thigs 
  - Productivity of officers is highly correlated with the number of licences/permissions they issue
  - Workers work between 8am~6pm and take a lunch break between 12~1pm.
- It seems consistent with the productivity of standard office workers because the number increases throughout noon. The peak is between 10 am to 12 pm but the number decreases during lunch break time. After the break, the number of applications issued increased from 1~3pm but kept decreasing again after 3 pm till the end of work time.
- If the above two assumptions are valid, then it is possible to think officers of business licences work normally.

#### Figure5: Hourly counts.
![https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/application_status_pi_chart.png](https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/application_status_pi_chart.png)
- It shows 80% of applications are issued.

#### Figure5: Hourly counts.
![https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/folderyear_line_.png](https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/folderyear_line_.png)
- This plot shows changes in number of each year's business licenses issued.
- There is an upward trend. Despite there are some big drops in 2020, the number got recovered in 2022. Which implies the economy is getting recovered from impact of covid-19 sowly. 

#### Figure5: Hourly counts.
![https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/pct_change_year_bar.png](https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/pct_change_year_bar.png)
- This plot shows same data as previous plot but in bar chart and shows percentage changes in number of licenses compared with preivious year.

## Part 2 Finding correlation between changes in number of licenses and mesurements of ecnomy

The data does not show whether or not the business owners respond to the economic circumstances.


![https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/corr_normal.png](https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/corr_normal.png)
- The plot shows there is not a strong linear relationship between 
- Assuming business owner apply for new licenses based on same year's economy.
- For example, if the economy is bad during the year, the owner might shut down the busienss, or suspend it.

![https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/cor_shift.png](https://github.com/shchuka555/vancouver_business_licence_analysis/blob/main/figures/cor_shift.png)

- The plot shows there is not a strong linear relationship between 
- Assuming business owner apply for new licenses based on previous year's economy.

![]()
![]()
![]()
![]()
![]()
![]()
![]()



## Conclusion

  - ## Results
    -  Binary logistic regression has a lower error rate than multinomial one.
    -  Both algorithms have lower accuracy in classifying non-negative tweets.
    - The unigram model approach treats some positive phrases as multiple negative words.
      - example: "without complained" -> "without" + "complained"
    - The approach with Tf-IDF misclassified sarcastic and negative tweet, which contains many positive words.
 
  - ## What's next 
    - The result which I found was quite surprising because there is almost no linear-relationship between measurements of economy and changes in number of licenses issued. Possible solution is finding non-linear relationship.

## Credits

Dataset from 
- [City of Vancouver Business licences: 1997-2012](https://opendata.vancouver.ca/explore/dataset/business-licences-1997-to-2012/export/?disjunctive.status&disjunctive.businesssubtype)
- [City of Vancouver Business licences: 2013-2023](https://opendata.vancouver.ca/explore/dataset/business-licences/information/?disjunctive.status&disjunctive.businesssubtype)


Used informatations from [Statistics Canada](https://www150.statcan.gc.ca/t1/tbl1/en/tv.action?pid=3310027001&pickMembers%5B0%5D=1.42&pickMembers%5B1%5D=2.1&cubeTimeFrame.startMonth=05&cubeTimeFrame.startYear=2022&cubeTimeFrame.endMonth=09&cubeTimeFrame.endYear=2022&referencePeriods=20220501%2C20220901)

