---
layout: post
title: 'Healthy Davis Together: data Science for health equity'
date: '2021-07-05 00:00:00 -0700'
categories: projects
---

In 2020, The city of Davis and UC Davis initiated [Healthy Davis Together](http://healthydavistogether.org) a comprehensive response to the Covid-19 pandemic.
This project included an executive committee at UC Davis that ran and supported the free PCR testing and communications strategy for the city of Davis.
I co-lead the modeling team with Miriam Nu&ntilde;o which was tasked with the data analysis and epidemic modeling for HDT.
We decided that the best way to serve the team was to produce detailed reports at the weekly cadence during the height of the pandemic.
This was a "wartime" approach that allowed us the flexibility of writing reports (as opposed to dashboards).
In all we wrote 11 such reports.
The following is an example of the demographic based analysis that we were able to do using the HDT testing data and other variables, such as the count of repeat testing.
Ultimately, this analysis (and prior ones) impacted our Spanish language outreach for HDT.


## Example Healthy Davis Together Data Report
### Weds 2-17-2021

# Quick Take

* Davis Latino/Hispanic positivity rate has decreased to 0.45% from 2% (based on 7 day average), we take a deeper dive into the Latino cohort  
* First-time visitors numbers stabilize to around 300/day while repeat tests are on the rise (number of tests taken by repeat visitors).  Each unique test taker has taken on average 2.52 tests since the start of HDT community testing.
* Overall, the Davis resident positivity rate has decreased to around 0.3% and there are no detected outbreaks, with the most active CBG having only 4/256 positive tests = 1.6% (which could happen at random with a very low infection rate).t


# Deeper Dive into the Davis Latino Cohort



* Davis resident positivity rate saw a spike in late January, driven by positive tests among tLatino/Hispanic Davis residents.  For a two week span almost half of the Davis residents that had tested positive had listed Latino/Hispanic as their ethnicity.
* This trend continues to reverse itself and the Davis resident Latino positivity rate is not down to 0.45% (7 day average). 
* The percent of tests that are taken by Latinos has begun to decrease again, but this may be caused by an increase in the number of non-Latino’s testing since the overall test rate is increasing still.
* Latinos getting tested are generally younger than their non-Latino counterparts, the median age of tested Latinos is 29 as opposed to 41 median age for non-Latinos.  Generally, Latinos tend to be younger in Davis than non-Latinos, with a census-based median age of 23 for Latinos and 29 for non-Latinos (median of medians by CGB)


#### Davis resident positivity rate for Latino/Hispanics (blue) and all (red)


![alt_text](/images/hdt_images/image1.png "image_tooltip")


Recall that Davis residents are those listing addresses within Davis CBGs.  Latinos are those listing ethnicity as Latino/Hispanic.


#### Latino Test Rate among Davis Residents (compared to population)


![alt_text](/images/hdt_images/image3.png "image_tooltip")


The above plot shows the percentage of tests for Davis residents that list Latino/Hispanic as ethnicity in the HDT community testing data (red) and the percent of the population of Davis.  Davis residents are those that list an address in a Davis census block group.


#### Age distribution for all of HDT testing for Latino and non-Latino

![alt_text](/images/hdt_images/image6.png "image_tooltip")

# Repeat Testers are on the rise while New Testers remains steady around 300/day

* First-time visitors numbers stabilize to around 300/day while repeat tests are on the rise (number of tests taken by repeat visitors).  The number of tests that are attributed to a repeat user has risen to over 1000/day.
* Each unique test taker has taken on average 2.52 tests since the start of HDT community testing.  75% have taken 3 or fewer tests, and the number of users that have taken x tests follows a power law distribution.
* Among the repeat testers the average time in between tests is around 12 days (this is based on a 7 day average).  This average was as low as 8 days previously, but recall that there were much fewer repeat testers then.
* Overall there are 27,953 unique users (first time tests) and among the first time tests the positivity rate is 2.54%.  There are 42,526 tests from repeat users with a positivity rate of 0.8%.  Of course, since the positivity rate is decreasing these numbers will be smaller if we look at more recent tests.


####  Number of tests that are a user’s first time (red) or a repeat test (blue)

![alt_text](/images/hdt_images/image2.png "image_tooltip")

#### Histogram of the number of tests taken by a user

![alt_text](/images/hdt_images/image4.png "image_tooltip")

#### Days since the last test for repeat users by test date (7 day moving average)

![alt_text](/images/hdt_images/image5.png "image_tooltip")

# In other modeling news

* Our team is working with the wastewater group to unify the analysis of the testing data sources and improve wastewater testing strategy.
* We are working on a mobility based network epidemiological model that should be available in the coming weeks - this should help to understand the impact of mobility and the spread of Covid-19.
* Many studies are in the works to assess the efficacy of non-pharmaceutical interventions, testing, and the impact of behavioral/lifestyle changes.  This includes government interventions, mobility pattern changes, university openings, and testing rates.
* We are working to get data on communications interventions, statewide testing, wastewater testing, and more.

The Modeling Team
