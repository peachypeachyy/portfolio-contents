# Finding correlations between gdp per capita and working hours per week.

## Description

This project is an academic project which involves finding a correlation between gdp per capita and number of working hours per week.
The general idea behind this is that there is a prejudice that undertaking more work would lead to higher income. The aim of this project is to validate that and check if truly does increase in number of working hours directly result in higher gdp per capita.

## Technologies used

    - R and R Studio 4.3


## Data source

    - Gapminder
    - World Bank data


## Methodology

The project involves 4 main tasks

    1. Data Cleaning and pre-processing
    2. Data visualization and trend identification
    3. Formulations of Linear regression equations to model the relationships
    4. Confirm the bias based on cluster analysis.


Link to the entire project is here : https://drive.google.com/file/d/1YWxdi-sM2qdCSpajVydotnmJwOCK_2Cr/view?usp=sharing


1. The Data Cleaning and pre-processing was mostly done in R itself using base libraries by creating functions and using `pivot_longer()` functions to transform data into columns for further processing

2. To identify trends, I categorized countries based on income levels, we could see some trends particularly with GDP, but with respect to working hours per week, it was choopy.

Following shows the gdp trends:

![My Image](https://github.com/peachypeachyy/portfolio-contents/blob/main/wrk_hrs_week_gdp_data_analytics/supporting_assets/gdp_of_countries.png)

Following shows the working hours per week trends:

![My Image](https://github.com/peachypeachyy/portfolio-contents/blob/main/wrk_hrs_week_gdp_data_analytics/supporting_assets/wrk_week_countries.png)



3. Due to the choppiness of working hours per week, we could use linear regression to create the equations and the relationship between the variables.

Following shows the linear equations between the variables:

![My Image](https://github.com/peachypeachyy/portfolio-contents/blob/main/wrk_hrs_week_gdp_data_analytics/supporting_assets/eqns_countries.png)


We can see the slope increases as we move from poorer countries to richer countries, but also we see that there is a negative correlation between the two variables.


4. We see from the cluster analysis as well, that we have 3 distinct clusters based on High Income, Low Income and Upper Middle Income. Each of them have a comparable difference in GDP per capita, hence we see High income countries as a cluster over 6, Upper middle income countries between 5.5 and 5.8 while lower income countries having a low average GDP under 4. It is also evident from the level of dispersion seen for the Average working hours of each cluster that justifies the low coefficient values as we move from Higher income countries to lower income countries. as seen here. The High income countries range from 3.6 to roughly 3.67 which is a small range compared to Upper middle income countries which range from 3.65 to roughly 3.85. We then further see a wider range in lower income countries where they range from roughly 3.3 till 3.9 which is the largest range. All the categories however had an increase in GDP per capita over the number of year.

Following is the cluster analysis :

![My Image](https://github.com/peachypeachyy/portfolio-contents/blob/main/wrk_hrs_week_gdp_data_analytics/supporting_assets/cluster_analysis.png)



## Conclusion

There is no evidence to state that there is a positive correlation between average gdp per capita in any of the countries compared to number of hours worked per week, i.e the more work produced each hour does not translate into an increase in gdp per capita. On the other hand, a decline is observed, and the decline is steeper as we move from Richer countries to Poorer countries.


## Learnings

In this project, I was able to wrangle data using R within R-Studio to transform and Identify relationships between different variables. I was then also able to dervice conclusions and use cluster inferencing to validate my results in R Programming Language.