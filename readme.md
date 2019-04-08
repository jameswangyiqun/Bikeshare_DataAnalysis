# Bikeshare Data Exploration

## Dataset

The data consists of information regarding 1.8 million trip records, including
trip start and end time, user type, user gender and age, trip route category. The dataset can be found in the
Ford GoBike official website [here](https://www.fordgobike.com/system-data), after downloading the zip file, 
I unzip them and append them to a pandas DataFrame.
I made some data cleaning:
1.from trip start time extract 'month','day','hour' to represent the time features of trip
2.from user birth year extract 'age'
3.from station information extract trip type: 'One Way' or 'Round Trip'
4.If user gender is null, I fill null by string 'Unknow'
5.change trip duration unit to minute

After cleanning, I saved the DataFrame to a csv file 'bay2018_clean.csv'

## Summary of Findings

In the exploration, I found that there was no relationship between trip duration and user age.
What ever I split the dataframe, by user type, user gender, trip type, day, the regression lines
are always parallel x axis, so that is mean, trip duration will not change by user age. I stopped here.

From the 'hour' feature, I found most trip occured at 8AM and 5PM, that is commuting time.
Also from the 'day' value, I found more trip occured on Monday to Friday. So I try to find what is diffrent
between commuting time and other time.

When I caculate the mean of duration, I found that, at Non-commuting time, the average trip duration is longer
than commuting time.
Next, I found what kind user take bike for going to work and home. Subscriber does.
Causal user usualy use bikeshare for travel, and take it for longer time in Non-commuting time.


## Key Insights for Presentation

For the presentation, I focus on the user feature which is influence the purpose of taking bikeshare.
Subscriber user usualy use bike for going to work and home on weekday commuting time, by One Way trip.
The casual user usualy use bike for travel on weekend, by Round trip. And he or she will not provide 
personal information probably.


