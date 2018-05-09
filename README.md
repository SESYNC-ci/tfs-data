
*Note: updated data files on 9 May 2018 correct a previous release*

README for Global_Food_System_Resilience_Indicators.csv

The data in “Global_Food_System_Resilience_Indicators.csv” were used for the analysis and to generate the figures in Seekell et al. (in revision). Complete methods for the development of the socio-economic and the production diversity indicators can be found in Seekell et al. (in revision). For the biophysical redundancy (or capacity) indicator we provide here only a short overview of the methodology, see the complete methods in Fader et al. (2016).

Three indicators relating to resilience in the global food system are provided for each country from 1992 to 2011 when data were available. Briefly, the three indicators presented are:


## 1) Socio-economic indicator (SE)

We calculated an index of socio-economic access to food based on (i) the *average income of the lowest 20% of each country’s income distribution* and (ii) the *average per capita food expenditure*. These can be viewed as key indicators in forming a domestic food price index. This index reflects resilience to short term changes in food prices. Estimates of the income of the lowest 20% of the population are based on several sources. Data for high-income countries are from the Luxembourg Income Study database (LIS Cross-National Data Center, 2016). Data for other countries were retrieved from the World Bank Development Research Group (Research at the World Bank, 2016) and are based on primary household surveys obtained from government statistical agencies and World Bank country departments. Estimates of the lowest 20% of the income distribution use the methods used in the World Bank’s PovcalNet models used to estimate rates of poverty (PovcalNet, 2016). These methods are described in detail at: http://iresearch.worldbank.org/PovcalNet/index.htm. 

### Criteria for interpolation of data for (i)

In order to cope with limited yearly availability on income distribution for some countries (notably in Africa), we reconstructed, when possible, the time series for a given country. To this end, we fitted a logarithmic curve to the available data in order to recover the time series for the period of interest (years beginning in 1992). We followed the below criterion for out-of-sample extrapolation and in-sample interpolation; when it was not met, we left the missing values.

At least 4 data points (years of data) had to be available in the source data, of which no more than one prior to 1990. This applies to 26 countries in our sample. 
For all other countries in our sample (70), we have at least 5 observations in the period 1992-2014.

As a result, the dataset for the socioeconomic indicator (for which we have data both for income (i) and food price (ii)) comprises 96 countries. 

We integrated the PovcalNet estimates with UN data (UN, 2016). Countries for which data was not available and that did not fulfil the above requirement have been excluded due to insufficient data.

### Aggregation into one indicator

We combined these two metrics into a single index by taking the ratio of income to food price. Indicator values approaching 1 from above suggest increasing trade-offs with other critical expenditures (e.g., housing) and reduced ability to make-up caloric deficits through food purchases. 

## 2) Biophysical capacity to produce food indicator (BioPysical)

We use the biophysical capacity indicator developed and described by Fader et al (2016). Please refer to this study when using the data and for the complete methodology, meaning, implication and applications of the measures as well as shortcomings of the calculation.

Fader et al. (2016) calculated three scenarios of biophysical redundancy (or as called in the present study “biophysical capacity”) considering a variety of definitions for resource availability and sustainable usage. We here use only the middle scenario where “managed grasslands are considered available, protected areas and areas worthy of protection are assumed to be unavailable for agricultural production, spare areas are considered to be 30% less productive than used areas, potential yields are assumed to be lower on unused areas than on used areas, precipitation and seasonality of precipitation are assumed to reduce accessibility of water resources by 10%–30% (depending on the variation coefficient of precipitation), environmental flow requirements are assumed to be lower than in the Rlow scenario but they are assumed to be met.” (Fader et al., 2016).  

The biophysical capacity indicator has four subcomponents: water, land, yield gap on used land, and yield gap on available fertile land. Fader et al. (2016) estimated unused freshwater resources based on data from the FAO AQUASTAT database. Unused resources were calculated as the total renewable freshwater resources minus water withdraws, environmental flow requirements, and the amount of water that is unavailable due to seasonal variability, rainfall intensity, spatial access, or lack of infrastructure. Unused arable land resources were estimated based on the HYDE 3.2 land use database (http://themasites.pbl.nl/tridion/en/themasites/hyde/) and the FAO Global Agro-Ecological Zones database. Unused arable land was calculated as total land area minus land area already used for agriculture (excluding pastures), land not suitable for agriculture, and land used for urban areas and other types of human settlement. Yield gap on used areas was estimated as the difference of actual yields for a given year and the maximum yields in similar areas given ideal fertilization and irrigation, multiplied by the used area. Finally, yield gap on unused areas was estimated similarly than in used areas, but assuming that potential yields on spare areas are 30% lower than on already used areas. The values for potential yields were extracted from Mueller et al (2012). For each factor, we compiled values for the years 1992-2011 that can be found in the excel file “FaderEtAl_2016_BiophysicalRedundancy_MiddleScenario.xlsx”. 

The values for each index were combined into an aggregate biophysical capacity measure by assuming that land and water were non-substitutable, but that yield gap was substitutable with these factors. In other words, increasing the amount of available farmland does not increase the biophysical capacity to produce food if there is not also available water. However, extensifying or intensifying (yield gap closure) can both (or either) be used to increase biophysical capacity. This index is scaled between 0 and 1 by calculating the amount of calories that can be produced with the redundant resources compared with population numbers in each year (FAO, 2015). All subcomponents are converted in an index between 0 and 1 indicating the theoretical amount of people that a country can feed with an adequate diet produced by redundant resources. Countries that have redundant resources for producing the caloric nutritional needs for at least 50% of its population for one full year were considered to have *high redundancy*. Countries with values between 25% and 50% were considered to have *limited redundancy*. And countries that have redundant resources for producing the caloric nutritional needs for less than 25% of its population have *very low redundancy*. Note that this refers to potential calories production *in addition* to current production.

## 3) Production diversity indicator (HIndex)

We applied the “h-index” from bibliometric analyses to evaluate total production and breadth of production (Hirsch, 2005). We applied this index to the food production and population data in the FAOSTAT database (FAO, 2015). First, we calculated the annual domestic production of each commodity in each country:

`Ci = Ki / Pj`

where Ki is the total kcal produced by a commodity in a given year and country (adjusted to units of kcal day-1), and Pj is the population of country j, giving Ci units of kcal day-1 person-1. Ki was determined using the FAO commodities database (given in units of weight) and using the FAO conversion factors to express Ki in kcal (FAO, 2016). For this analysis, we only considered primary food products (see main text for justification). Then, we calculated each country’s h-index for the years 1992-2011. 
To calculate the h-index for a combination of country and year, all Ci were ordered from greatest to least and given a rank depending on their order in this sequence (i.e. the commodity with the highest Ci is given a rank of 1, the commodity with the second highest Ci is given a rank of 2, and so on). Then, we calculated the h-index as the largest Ci for which the corresponding rank does not exceed Ci. In other words, an h-index of 20 would indicate that a country’s production stream includes 20 commodities that produce at least 20 kcal per capita per day, but does not have at least 21 commodities that produce at least 21 kcal per capita per day. Whereas an h-index of 40 indicates a country’s production stream includes 40 commodities that produce at least 40 kcal per capita per day each, but not 41 commodities that produce at least 41 per capita per day. Therefore, a country can only score a high h-index value if it has a production stream that has high production per capita and is also diverse. For example, a country that produced 1500 kcal per capita of corn, but then only 10 kcal per capita of 5 other commodities would have an h-index of 5 and would be highly susceptible the perturbations that reduce the productivity of corn more than other crops. 

## References

* Fader, M, MC Rulli, J Carr, J Dell’Angelo, P D’Odorico, JA Gephart, M Kummu, N Magliocca, M Porkka, C Prell, M Puma, Z Ratajczak, DA Seekell, S Suweis and A Tavoni (2016) Past and present biophysical redundancy of countries as a buffer to changes in food supply. Environmental Research Letters, 11: 055008.
* Food and Agriculture Organization (2015) FAOSTAT database, Available at: http://faostat3.fao.org/faostat-gateway/go/to/home/E, accessed 02.05.2015
* Food and Agriculture Organization (2016) Nutritive Factors, Available at: http://www.fao.org/economic/the-statistics-division-ess/publications-studies/publications/nutritive-factors/en/, accessed 21 Nov. 2016
* Hirsch, JE (2005) An index to quantify an individual’s scientific research output. Proceedings of the National Academy of Science U.S.A., 102: 16569–16572.
* LIS Cross-National Data Center In Luxembourg (2016). Available at: www.Lisdatacenter.org. Accessed 18 Nov. 2016.
* Povcalnet platform. Available at www.Iresearch.worldbank.org. Accessed 18 Nov. 2016.
* Research at the Worldbank. Available at: www.Econ.worldbank.org. Accessed 18 Nov. 2016.
* Seekell, DA, J Carr, J Dell'Angelo, P D'Odorico, M Fader, JA Gephart, RP Korzeniewicz, M Kummu, N Magliocca, M Porkka, C Prell, M Puma, Z Ratajczak, MC Rulli, S Suweis and A Tavoni. Resilience in the global food system. In Revision at Environmental Research Letters.
* UN data. Additional poverty data from http://unstats.un.org/unsd/snaama/Introduction.asp and UNU WIDER WIID, 3.0b release. Accessed 18 Nov. 2016.




