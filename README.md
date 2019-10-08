# SMU-Project1-Group3
# ANALYZING UBER TRIPS OCCURED IN NEW YORK CITY

## SUMMARY
Uber has become hugely popular in New York, and its trips outpaced yellow taxis for the first-time last year. There are about 65,000 vehicles affiliated with Uber in the city, which provide more than 400,000 trips per day, according to the Taxi and Limousine Commission. Objective of this study is to provide an analysis of Uber Rides in New York City.

## DATA PREPARATION AND EXPLORATION
Data is retrieved from AWS. Data set includes the trips occurred in New York city between September 2014 and September 2015. Data set consists of 31 million rows (1,5 GB size). Random sample of 100 thousand rows of data is used for analysis. 4078 rows of data is ignored because of missing values in the data set. No duplicate values are found in the dataset. In total, 4% of the records are ignored. 96% of original data is retained for data analysis.

## QUESTIONS  & HYPOTHESES
- What time of the day is Uber ride requested more?
- Which date of the year is Uber ride requested more?
- What is the relationship between trip distance and trip duration?
- What are popular pick-up and drop-off locations?
- How many rides start and end in the same neighborhood?
- What is the relationship between staying in the same neighborhood and distance?
- What is the relationship between leaving the neighborhood and distance?

## DATA ANALYSIS & DATA VISUALIZATION

#### Distance vs Distribution: 
We hypothesized that trip duration and trip distance are highly correlated and estimated an R2 of at least 0.95. However, the data does not support this with an R2 of 0.41 calculated on a 100,000 entry set. Even so, the p-value of the dataset was found to be less than 0.05 (at 0.00) and is therefore significant and we reject the null hypothesis that trip duration and trip distance are not related. We induce that, particularly in New York City where the data hails, heavy traffic congestion in the nucleus of a city leads to a drawdown in the average distance per unit of time compared to more distal areas that allow drivers to travel greater distances at a more rapid cadence. Therefore, in certain areas of extreme traffic minimal distance was covered per unit of time, while others allow for a more steady and swift flow. Also, at the recommendation of our instructor, we capped the upper bound of duration at the third quartile to exclude substantive outliers, one particular point asserting that a trip lasted over 7 continuous days. Additionally, we truncated the data to only include Uber trips that lasted longer than two minutes as many rides were logged as lasting zero seconds while simultaneously making headway with regard to distance. Assuming that teleportation is least likely to happen in a gridlocked New York City artery if anywhere, these points were also removed from our figure.  
