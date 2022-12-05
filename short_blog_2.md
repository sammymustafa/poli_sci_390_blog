# Short Form Blog 2

Free and fair national elections are one way people attempt to prevent corruption from polluting their country’s government. One attempt to this includes making national elections free and fair for the people. One may think that this would allow for the people to elect high ranking officials that would uphold the country in a way they want, with low levels of corruption. However, this assumption may be controversial, as seen in literature ([Bacchus & Boulding, 2021](https://onlinelibrary.wiley.com/doi/10.1111/gove.12598)), and thus cannot be made without studying the association between these variables.  

Thus, the Varieties of Democracy (V-Dem) dataset ([Coppedge et al., 2021](https://www.v-dem.net/static/website/img/refs/codebookv111.pdf)) was utilizied to study the association between the `v2elfrfair_osp` and `e_wbgi_cce` variables. The former variable (Pemstein et al., 2021) considers all the aspects of the pre-election, election, and post-election periods to index fairness throughout the process while the later variable (Kaufmann et al., 2016) is a World Bank governance indicator that measures the perception of various aspects of corruption, all defined as utilizing public power for private benefit. 

The data include these indexes from the years 1996 to 2020 of various regions around the world. Thus, visualizating the correlation and trends underlying these two variables can reveal whether or not having free and fair elections has been consistently enough to produce countries with governments of low corruption. 



## Visualization 1:
![](/blog2_trend.png)

The first visualizations displays the general trend between the levels of election fairness and government corruption. This contour plot displays the trend sway of the data. It can be seen there is more control of corruption or less corrupt governments when there are more fair elections. However, the plot displays how the increase in less corruption from the least to most fair elections is not that insignificant until reaching the most fair elections. The magnitude of the positive slope is quite low until reaching the most fair elections, where the slope becomes much more significantly steep towards lower levels of corruption. 



## Visualization 2:
![](/blog2_map.png)

The next visualization uses the `geom_sf()` function to highlight the different level of corruption across the world. Notably, it can be seen that a lot of corruption identified from the dataset tends to be within Africa, Asia, and South America while lower levels of corruption are found in North America and Europe. However, it is important to note that certain countries are not included in this dataset, most notably China; these absences may cause a shift in the data. This emphasizes that the correlation between corruption levels and election fairness should be studied more specifically in different regions to allow for a better comparison to be made across the world.



## Visualization 3:
![](/blog2_region.png)

With this, the data was facetted by the six regions identified by the dataset to allow for more concrete correlations to be identified by region. The distributions graphed include the levels of election fairness and government corruption across the years from countries of the specified region; a linear regression shows the general trend between the indexes. It is evident that North America and Western Europe have high levels of election fairness and low levels of corruption to the extent that the election fairness index doesn't really determine corruption levels as the government, represented by the almost zero slope. The data for the other regions, however, display that there is not really a large increase in corruption control due to election fairness. This is most notably seen by the low magnitudes of the slopes for the Sub-Saharan Africa and Latin America and the Carribean regions. 



## Visualization 4:
![](/blog2_heatmap.png)

The last visualization is a heatmap between the levels of election fairness and corruption by region. The heatmap does a very good job in showing that there is really no evident change in government corruption level until elections reach a very high level of free and fairness, as the colors do not change until reaching this level. However, it does also highlight that all the data for the North American and Western Europe region is from a high level of election fairness, which means that the index for corruption control may be skewed to account for the high proportion of very fair elections in this region. 



## Conclusion

Overall, these data and visualizations highlight that election fairness cannot always be tied to levels of government corruption. This means that more work in addition to election fairness has to be done to ensure that governments are not corrupt. However, this requires further analysis with data that may not be skewed to account for the high levels of election fairness and low amount of corruption observed in North America and Western Europe. 

Moreover, it would be interesting to study this data by year and, more specifically, by country to identify more trends. This was hard as the trends witnessed were very scattered due to national elections occurring at different times/interval of years for different countries so accounting for how these confounding variables affect this correlation would be interesting. For examples, studying how corruption levels have changed for countries that have taken greater efforts to make the election process more fair would underscore this trend further.
