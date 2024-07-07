# BakerysalesEDA

To be able to undestand the sales pattern of a bakery business , it helps business owner to better positision their business strategy. Bakery Owner now can make data-driven decision based on their history sales data. The sales EDA analysis will benefit marketing team in formulate more effective marketing strategy.

Data source : https://www.kaggle.com/datasets/matthieugimbert/french-bakery-daily-sales/data

Problem Statement : To get an insight on the sales pattern ,which enable us to answer questoion likes ; 
                    a. what is the most-sold menu?
                    b. which season during a year that contribute the highest sales?
                    c. when is the session of the day that made the highest sales ?

Data Profile:
a. dataset contains 234005 rows of sata and 7 columns ( index,dates, time, ticket_numbers, article, Quantity ,unit_price)

Methodology:
a. Convert the spring value to capitalize each word for article 
b. Rename the columns so that it is easier to understand the meaning ( ticket_numbers : Transaction ID; article:Item; unit_price:Price)
c. Change the data format for date , time to datetime format , and Transaction ID , Price and Quantity to numeric format
d. Remove the euro sign from the price column to enable math calculation later
e. Add columns that split date to month, day and weekday and time to hour
f. Check for null and duplicate value. There is no null or duplicate value, no actiona needed
g. Remove negative quantity and price from the dataset as it is due to error in recording 
h. As a result , the final dataset has (233973 rows of data and 15 columns）

EDA Finding:

We have the top 10 most-sold-items from the bakery and the revenue made by month and years during the record period. The no.1 sold -Traditional baguette from the bakery , shows that the local is very much depending on this kind of pastry for daily energy provider. Comparing to other different flavored pastries , plain traditional baguette allows it to be taken with other jams or filling. This bakery recorded a better revenue during the second half of the year , for both 2021 and 2022, in which August being the best month while january being the worst month.

From the Corr Heatmap, we could see some linear positive relationship between , Quantity , Price , and Revenue . However Corr did not tell us the causal relationhip between these variables , for example ( Transation Id and Year-0.8611).

Quantity and Revenue - 0.5114, both has a medium positive relationship Prive and Revenue- 0.7378- it has to be positive related since with higher price , the bakery can generate higher revenue if quantity is not affected

Weekend is as a whole generate better revenue compare to weekday, with Sunday recorded the highest among the weekdays. The bakery can look into stratery to boost the sales for middle of the week , ( Wed gives the lowest revenue)

It is interesting to see that most of the sales was done during the morning session from 8-11am , the sales peak at 11am , and slowly coming down after lunch hour. The sales improve slightly during 4pm-6pm and then slow down drastically . The hourly sales pattern could provide some hindsight to the bakery in setting their business hour. The hour after 6pm contribute very litter sales , maybe the bakery can consider to end their business by 6pm . 

As the percentage of sales after 7pm is of 0.44% of the total sales record , the bakery could consider to close the business by by 7 pm instead of open until so late. This can help them to save the man power and utility cost and make better use of it in boosting the sales during other time of the day.

From the calculation ,we also realized that the top 10 menu items constitutes 47% of the total sales (total unique menu item=149 ) thus , it is worth to delve into those less sold item and decide whether to discontinue or improvise. The bakery can also design a package sale that tie up 2 or more menu item together, which can help to boost those less sold menu item


