# Visualization Blog 2

Here, I utilized data from the New York State Database that details the hourly traffic on MTA bridges and tunnels since 2010 ([MTA, 2022](https://data.ny.gov/Transportation/Hourly-Traffic-on-Metropolitan-Transportation-Auth/qzve-kjga)). With this data, I hoped to visualize the amount of traffic, measured by the number of vehicles passing through the tolls, and consider uncertainity within my graphics. 


# Traffic by Hour
Initially, I knew that the traffic would vary heavily by hour, in which rush/commutting hours would represent the peaks in movement across New York. However, I hoped to consider the 95% confidence interval and show this from the lower and upper bound error bars to see if these differences in the mean traffic observed per hour was insignificant considering the precision of the value. Thus, I created a function to calculate the upper and lower bounds; however, I needed to calculate the mean and standard error (from the count of values and standard deviation) to input into this function to input into the `geom_errorbar` aesthetic.  

With these bars present, one can see that these differences are still significant because when even considering for their measure of preicision, the values and the error bars do not overlap, especially during the early and mid-day. In addition, this effect is not as present in the toll data, most likely because the amount of people using tolls is much less than that with E-ZPass. 

![Hour Traffic](/hour_traffic.png)


# Traffic by Year
From this, I hoped to visualize the amount of traffic per year using the raincloud plot utilizing `stat_halfeye` and `stat_dots`. I needed to filter my data a bit to make this possible so I focused on one plaza/bridge that I have been to (plaza_id = 24 = Henry Hudson Bridge), E-ZPass data as this is most common as seen above, during the peak hour of 3:00 PM as seen above, and during the month of June. I wanted to look at the data from the past five years so I looked at the data since 2018. Thus, I used a specification in the `.width` aspect of  to consider the IQR and 95% data range. 

With this, we could understand and compare the distribution of traffic across these years. From the data, we can see the drop in traffic from 2020, which is most likely due to the COVID-19 pandemic. However, it was suprising to see the spike in traffic in 2021 and 2022 compared to the years prior to the pandemic. Thinking about it more, this may be due to less people taking public transportation and more people relying on driving to work in order to avoid contact with other individuals for health concerns but in addition to the safety concerns that public transportation has posed in the last two years. 

![Year Traffic](/year_traffic.png)
