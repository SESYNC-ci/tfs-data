README for Global_Food_Security_Indicators.csv

The data in this file were used for the analysis and to generate the figures in Seekell et al. (in review).
Complete methods for the development of the three indices can be found in Seekell et al. (in review) and Fader et al. (2016) Past and present biophysical redundancy of countries as a buffer to changes in food supply. Environmental Research Letters, 11 055008.

Three indicators relating to resilience in the global food system are provided for each country from 1992 to 2011 when data were available. 
Briefly, the three indicators presented are: 

1) Socio-economic indicator (SE) 
We calculated an index of socio-economic access to food based on the average income of the lowest 20% of each country’s income distribution and average per capita food expenditure as key indicators in forming a domestic food price index. 
This index reflects resilience to short term changes in food prices. 
Estimates of the income of the lowest 20% of the population are based on several sources. 
Data for high-income countries are from the Luxembourg Income Study database. 
Data for other countries were retrieved from the World Bank Development Research Group and are based on primary household surveys obtained from government statistical agencies and World Bank country departments. 
Estimates of the lowest 20% of the income distribution use the methods used in the World Bank’s PovcalNet models used to estimate rates of poverty. These methods are described in detail at: http://iresearch.worldbank.org/PovcalNet/index.htm. 
We combined these two metrics into a single index by taking the ratio of income to food price. 
Indicator values approaching 1 from above suggest increasing trade-offs with other critical expenditures (e.g., housing) and reduced ability to make-up caloric deficits through food purchase.

2) Biophysical capacity to produce food indicator (BioPysical)
We use the biophysical capacity indicator developed and described by Fader et al (2016). 
In this indicator unused freshwater resources were estimated based on data from the FAO AQUASTAT database. 
Unused resources were calculated as the total renewable freshwater resources minus water withdraws, environmental flow requirements, and the amount of water that is unavailable due to seasonal variability, rainfall intensity, spatial access, or lack of infrastructure. 
Unused arable land resources were estimated based on the HYDE 3.2 land use database (http://themasites.pbl.nl/tridion/en/themasites/hyde/) and the FAO Global Agro-Ecological Zones database. 
Unused arable land was calculated as total land area minus land area already used for agriculture (excluding pastures), land not suitable for agriculture, and land used for urban areas and other types of human settlement. 
Finally, yield gap was estimated as the difference of actual yields for a given year and the maximum yields in similar areas given ideal fertilization and irrigation minus actual production, multiplied by the spare and used areas. 
These maximum values were estimated following the approaches of Mueller et al (2012). 
For each factor, we compiled values for the years 1992-2011. 
Fader et al (2016) considered a variety of scenarios representing different levels of availability for unused land and water resources. For the present analysis, we consider values from the middle scenario. 
The values for each index were combined into an aggregate biophysical capacity measure by assuming that land and water were non-substitutable, but that yield gap was substitutable with these factors. 
In other words, increasing amount of available farmland does not increase biophysical capacity to produce food if there is not also available water. 
However, extensifying or intensifying (yield gap closure) can both (or either) be used to increase biophysical capacity. 
This index is scaled between 0 and 1, with values less than 0.5 indicating limited water, land, or productivity redundancy.

3) Production diversity indicator (HIndex)
We applied the “h-index” from bibliometric analyses to evaluate total production and breadth of production. 
First, we calculated the annual domestic production of each commodity in each country:
Ci = Ki / Pi
where Ki is the total kcal produced by a commodity in a given year and country, and Pi is the population. 
Ki was determined using the FAO commodities database (given in units of weight) and using the FAO conversion factors to express Ki in kcal. 
For this analysis, we only considered primary food products. 
Then, we calculated each country’s h-index for the years 1992-2011. 
To do this, all Ci were ordered from greatest to least and given a rank depending on their order in this sequence (i.e. the first ordered Ci has a rank 1, the second has a rank 2, and so on).
Then, we calculated the h-index as the largest Ci for which the corresponding rank does not exceed Ci. In other words, an h-index of 20 would indicate that a country has 20 commodities that produce at least 20 kcal per capita, whereas an h-index of 40 indicates a country has 40 commodities that produce at least 40 kcal per capita each. 
A country can only score a high h-index value if it has a production stream that has high production per capita and is also diverse. For example, a country that produced 1500 kcal per capita of corn, but then only 10 kcal per capita of 5 other commodities would have an h-index of 5.
Squaring the h-index leads to a threshold value that can be used to evaluate relative levels of resilience.
Specifically, an h-index greater than ~43 indicates very high resilience on this axis because 43 commodities × 43 kcal/commodity = 1849 kcal, which is close to thresholds previously used to delineate low dietary energy availability.



