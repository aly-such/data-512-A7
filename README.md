# A.7. Final Project

## Goal:
The goal of this assignment was to complete our proposed extension of assignment A4 that was outlined in assignment A5. An analysis of Covid data in San Diego county as well as other California counties was done to get a better understanding of tranmission rates as well as how the vaccine might affect rates. The analysis probed two research questions:
1. Did the vaccine have an effect on COVID transmission rates in San Diego County?
2. Was there a difference in COVID case rates and vaccination rates between San Diego County and other counties in California?
Within the analysis, time-series charts and heat maps were created, and t-testing was conducted to get some answers to these questions.


## Data Sources:
* COVID Act Now: https://apidocs.covidactnow.org/#register
* License for Covid Act Now Data: https://creativecommons.org/licenses/by-nc-nd/4.0/
* California's County Populations: https://www.california-demographics.com/counties_by_population
* Personal License: https://github.com/aly-such/data-512-A7/blob/main/LICENSE

## Data Descriptions:
### https://api.covidactnow.org/v2/county/CA.timeseries.csv:
This will only include the columns used in my analysis.
* date - date, this data table was a time-series dataframe which track the cumulative metrics each day
* country - str, country of county
* state - str, state of county
* county - str, county (only includes California counties for this analysis)
* fips - int, identification ket for county
* cases - int, cumulative number of cases up to that date
* deaths - int, cumulative number of deaths up to that date
* vaccinations - int, cumulative number of completed vaccinations up to that date

### California County Populations:
* County - str, name of county found in California
* Population - int, population of the county named

### Some other fields that can be found in the dataframes:
* Daily_Cases - int, (today's case amount - yesterday's case count), the daily number of cases for that day
* Moving_7_Day_Avg - int, takes Daily Cases and smooths out the result by taking a 7 day moving average
* Daily_Vax - int, (today's vaccine amount - yesterday's vaccine count), the daily number of completed vaccines for that day
* Moving_7_Day_Avg_Vax - int, takes Daily Vax and smooths out the result by taking a 7 day moving average
* Case_Rate - int, (Daily_Cases / Population), the daily rate at which people are infected for that county and date
* Avg_Rate - int, (Moving_7_Day_Avg / Population), the 7 day moving average of the daily case rate for each county and date
* Vax_Rate - int, (Daily_Vax / Population), the daily rate at which people are vaccinated for that county and date
* Avg_Vax_Rate - int, (Moving_7_Day_Avg_Vax / Population), the 7 day moving average of the daily vaccination rate for each county and date

## Notes:
You must register through COVID Act Now to get an API key to access the datasets they have. They can be retrieved in either json or csv format.
