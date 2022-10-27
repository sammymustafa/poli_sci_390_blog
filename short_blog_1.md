# Short Form Blog 1

Trips to the hospital are inevitable parts of most people's lives, whether it be for themselves or friends or family. However, the care that is received is not always the same. There are implicit biases and disparities present within the medical field that make treatment harder for certain groups. Particularly, it has been shown that a patient's race plays a big role in how they are treated in the hospital which subsequently affects their long-term outcomes. 

This is a topic that has been studied and addressed a countless number of times within the medical field to no avail. Racial disparities are present in who receives a mechanical heart pump or heart transplant, where white women are twice as likely as black women to receive these treatments ([NIH, 2022](https://www.nih.gov/news-events/news-releases/nih-supported-study-finds-racial-disparities-advanced-heart-failure-treatment)). This is as much of a problem during COVID such as how Black veterans were less likely to receive advanced COVID-19 therapies ([Kime, 2022](https://www.military.com/daily-news/2022/10/25/fewer-black-vets-got-advanced-covid-treatments-va-hospitals-during-pandemic-study-finds.html)). Overall, the effect of race in the healthcare industry is not because these populations "lack access to health care" but because of the "uncomfortable reality" in which these populations are not treated in the hospital as well as other populations ([Bridges](https://www.americanbar.org/groups/crsj/publications/human_rights_magazine_home/the-state-of-healthcare-in-the-united-states/racial-disparities-in-health-care/#:~:text=NAM%20found%20that%20%E2%80%9Cracial%20and,physicians%20give%20their%20black%20patients)). 

While the effect of race on treatment is known, I thought it would be interesting to see if these racial minorities are also burdened with greater hospital discharge costs; that is, I think racial minorities have to deal with higher costs for worse treatment. Thus, I acquired the "Hospital Inpatient Discharges (SPARCS De-Identified): 2019" ([SPARCS, 2019](https://health.data.ny.gov/Health/Hospital-Inpatient-Discharges-SPARCS-De-Identified/4ny4-j5zv)) dataset from New York State's Health Database (https://health.data.ny.gov/). 

This is a great and official database detailing various details of over two million hospital discharges from 2019; in addition to hospital treatment charge, the database reveals factors like the hospital cost, illness severity, length of stay, gender, and insurance utilized for treatment. With this, it is possible to study any associations and additional inequities present within the medical field's treatment of racial minorities. While the database could have included more detailed descriptions of race and ethnicity, it is still useful in differentiating between the majority white population of New York State. In addition, it would have
been nice to have a database encompassing this data among other years to see if there has been any change in discharge costs by race every year; previous years' data is also available but also contains over two million patient discharges so this may be a little to much data. 



## Visualization 1:
![](/blog1_cost.png)

The first visualization depicts the difference between the mean treatment cost for the hospital vs. the mean discharge charge for the patient by race for various lengths of stay. First, I aimed to see by how much hospital up-charge patients for their services, especially minorities. Next, I aimed to see by how much does this up-charge change with more days in the hospital. Lastly, I hoped to study differences between these two points among the different races detailed by the database.

Thus, I graphed the hospital charge as a solid line and the hospital costs as a dashed line to differentiate between these two values. In order to plot both sets of data on the same graph, I had to pivot the data longer and use linetype to differentiate between each value. Then I used different colors for these lines to differentiate the data by each racial group. 

It is evident to see that the hospital costs are much less than the hospital charges. Moreover, this up-charge seems to grow exponentially as the patient spends more and more days in the hospital. More importantly, the colors indicate how Multi-racial and patients described as Other Race had notably higher mean hospital charges. This shows that despite being in the hospital for the same amount of time, certain racial minorities have to pay more for their treatment than the racial majority. It was also interesting that they had higher mean hospital costs; while this may be because physicians are taught based off of information produced by mainly white individuals and may utilize more resources to approach minorities because there is more unknown, this should not be the case and should push for further representation in medical education.



## Visualization 2:
![](/blog1_severity.png) 

Next, I wanted to look at whether or not this observed difference in treatment cost was because of the severity of the illnesses these patients had. From this, I wanted to see the effect of both the severity of illness and race on the mean hospital charge for the patient.

In order to study this, I used a heatmap which ranged from blue representing the lowest cost, yellow being the middle cost, and red being the greatest cost. I filtered the data so the greatest values studied was a $100,000 hospital stay in order to exclude any outliers. 

The results of the heatmap confirmed what was previously seen, in which the racial minorities pay more for these treatments than the racial majority. This is most evident in the multi-racial column where each square is a bit darker than the rest in its corresponding row. Interestingly, this data shows that Black/African American patients have greater mean hospital charges than white individuals in more major and extreme illnesses. This may have not been observed in the first visualization due to the lack of this filter from outliers, but these further confirms the thesis that despite these racial inequalities in the healthcare industry, minorities have to face a greater financial burden.



## Visualization 3:
![](/blog1_age.png)

Continuing on, I thought it would be interesting to see if this observed higher mean hospital charge for racial minorities is present in all or in specific age groups. With this, I wanted to study the distribution of costs across these age groups among the different races using a violin plot. Since this is quite a bit of data, utilizing color in addition to the y-axis helps differentiate between the age groups.

It seems like younger patients have greater hospital charges for racial minorities compared to the racial majority. By contrast, the distribution of the eldest white age group is the largest and seems to be the source of a great amount of these reported hospital charges. With older populations, you would assume they experience more major and extreme illnesses which subsequently cause greater hospital charges, but from the heatmap from before we can still see that Black populations pay more than white populations for these types of treatments. This further suggests the inequality in hospital charges for racial minorities.



## Visualization 4:
![](/blog1_county.png)

Lastly, I wanted to expand this discussion of racial inequalities in the hospital to those enforced due to location. New York City is one of the most diverse but also racially segregated cities, even just by borough ([Baruch, 2017](https://www.baruch.cuny.edu/nycdata/income-taxes/med_hhold_income.htm)); this ties into funding and resource availability which can bring about negative effects in healthcare. By studying the differences in the mean hospital charge for each race by NYC borough, we can understand if location contributes to these racial inequities in the medical field. In addition, differentiating by medical and surgical-related treatments can help us determine if these disparities are due to a certain type of treatment. The way in which these boroughs are leveled in increasing income order makes it easier to see if there are any disparities in these treatment charges.

The way that the boroughs with the highest (Manhattan) and lowest (Bronx) mean income have the greatest mean medical and surgery charges for mostly every race shows how areas with people from lower financial backgrounds have to pay as much as areas with people from higher financial backgrounds. While most every racial minority seems to have a high mean hospital charge in the Bronx, it is interesting to see that white patients face greater hospital charges in the Bronx compared to Manhattan. While this goes against the thesis, minorities are paying a greater hospital charge in the borough with the greatest income, which also that with a majority of white individuals, suggesting that racial disparities are causing them to be further charged for these services. 


## Conclusion

To conclude, the data presented suggest that racial minorities seem to face racial inequalities in not only their hospital treatment but as well as their financial obligation to these treatments; here, we studied this in respect to variables like location, age, and illness severity. Minorities are paying more to be treated with bias and racial disparities that hurt them even more. While certain parts of these data and visualizations could have been enhanced, such as studying these realtions with insurance types, incorporating the ethnic make-up of these counties, etc., the data seem to be enough to highlight the financial burden that racial minorities have to carry from the medical field.
