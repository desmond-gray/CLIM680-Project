# 30-Year Precipitation Analysis of Virginia
 
### Desmond Gray
#### CLIM 680 - Fall 2022

[Project Proposal](https://desmond-gray.github.io/clim680_project_proposal/)

## Introduction

My initial proposal was to compare the difference between coarse GPCP precipitation data from stations and satellites with 
higher resolution ERA5 data that has been processed through a model. I will be comparing the grids to show how the points
differ when calculating climatology and anomalies. Due to covering such a small area, using the low resolution GPCP dataset did not make sense.
Therefore, I have shifted my focus to analysing total precipitation in Virginia due to it being the region most relevant to our class. I will assess
the patterns of precipitation in this area over a long timescale and make interpretations about my findings.

## Data

The datasets used in my project is The [ERA5 Global Reanalysis](https://www.ecmwf.int/en/forecasts/datasets/reanalysis-datasets/era5) provides hourly estimates of a large number of atmospheric, land, and oceanic climate variables from Jan 1959 to present.  It is on a 30km grid. ERA5 combines vast amounts of historical observations into global estimates using advanced modelling and data assimilation systems. Because of the size of this data set, I will only be working with the state of Virginia, while focusing on the variable of total precipitation (mtpr) between the years of 1980-2009. I chose the latitude and longitude ranges of 84W to 74W and 36N to 40N.

## Code Description

### [GroupBy](https://desmond-gray.github.io/CLIM680-Project/ERA5_GroupBy.ipynb)

The yearly average of daily precipitation values is represented by a 30-year climatology plot for Virginia. This was created using the groupby function to separate the data by year, and then applying this to the pyplot package in matplotlib to display the monthly data on a 6 row, 5 column plot. This allows me to display the yeary changes in average daily precipitation values and determine which years show the least and greatest precipitation. Figure 1 displays this 30-Year Climatology plot, with mean precipitation values fluctuating greatly across the entire state.

![era5_groupby.png](https://desmond-gray.github.io/CLIM680-Project/era5_groupby.png)
Figure 1: 30-Year Climatology Plot for Virginia


### [Aggregates](https://desmond-gray.github.io/CLIM680-Project/ERA5_Aggregates.ipynb)

I calculated the mean daily precipitation values for the state throughout my sliced timespan in an attempt to pick up trends during this period. Figures 2 and 3 display a basic line plot and contour plot the mean total precipitation rate.

![era5_agg1.png](https://desmond-gray.github.io/CLIM680-Project/era5_agg1.png)

Figure 2: Average Daily Precipitation Rate for Virginia (1980-2009)



![era5_agg2.png](https://desmond-gray.github.io/CLIM680-Project/era5_agg2.png)

Figure 3: Average Daily Precipitation Rate for Virginia (1980-2009)



### [Anomalies](https://desmond-gray.github.io/CLIM680-Project/ERA5_Anomalies.ipynb)

Next, I decided to plot anomalies for specific areas of interest. I checked 3 regions of the state that included the cities of Fairfax in northern Virginia, Norton in southwest Virginia, and Virginia Beach in the Southeast. I started by setting coordinates for each city and creating line plots of all of their mtpr values over the timespan. Then, to to display anomalies, I subtracted the monthly average mtpr values for the entire state from the original values. I repeated this process for each location to get an idea of how the anomalies would compare in locations of different topography.


### [NAO Composite](https://desmond-gray.github.io/CLIM680-Project/ERA5_Composite.ipynb)

I decided to create my composite with the North Atlantic Oscillation, due to it being geographically closest index to my location of interest that I was able to find. I splie it into 3 arrays for the positive, negative, and neutral phases of the NAO. I also increased the threshold of values to be +/- 0.5 for each phase in order to glean more significance from their correlation (Figure 4). The composite is focused on Spring Months (MAM) due to my research telling me that the likely rainy period for Virginia is March - November. Next, I alignined the NAO phase arrays so that they were on the same timescale as my dataset and finished by matching my anomalies with each respective phase of the NAO (Figure 5). After completing the composite, I performed a t-test to show the significance between the index and my anomalies. I performed the test between Positive and Neutral NAO Values, with a p-value of 0.05, and plotted the areas of significance with dots (Figure 6).

![era5_comp1.png](https://desmond-gray.github.io/CLIM680-Project/era5_comp1.png)

Figure 4: Spring NAO Phases 1950-2020



![era5_comp2.png](https://desmond-gray.github.io/CLIM680-Project/era5_comp2.png)

Figure 5: Daily Precipitation Anomalies During NAO Phases (1980-2009)



![era5_comp3.png](https://desmond-gray.github.io/CLIM680-Project/era5_comp3.png)

Figure 6: Composite Precipitation Anomaly Differences between Positive and Neutral NAO Phases



### [Function](https://desmond-gray.github.io/CLIM680-Project/ERA5_PythonFunction.ipynb)

I created a simple python function to convert the units of my precipitation data from kg/m2/s to mm/day.

### [Linear Regression](https://desmond-gray.github.io/CLIM680-Project/ERA5_LinearRegression.ipynb)

I also calculated the linear regression by using the NAO climate index and grouped it by Spring seasonal months (MAM). Next, I sliced the anomalies by year and set the climate index as the independent variable and my dataset as the dependent variable. Then I calculated the coefficient at every location within the state and plotted the spread (Figure 7).

![era5_linreg1.png](https://desmond-gray.github.io/CLIM680-Project/era5_linreg1.png)

Figure 7: Linear Regression between Spring NAO and Daily Precipitation Anomalies



## Results

When looking at the 30-year climatology plot, Virginia appears to go through about one very rainy year (>4mm/day) every decade, followed by relatively dry years (<3mm/day). The anomalies in all regions showed very little indication of trending in either direction. Regression analysis also indicates that none the NAO phases (positive or negative) have much impact on Virginia precipitation clmatology and anomalies, as there is very little correlation within this regression coefficients throughout the state.


## Summary

This project gave me good insight into the precipitation climatology of Virginia over a 30 year span. I learned that the NAO has little if any correlation to the total precipitation in Virginia or its anomalies. I would like to further tmy research by finding another index that my be more applicable to my geographical location, as well as diving more into how different topographical regions within the state are correlated to their precipitation rates.


## Conda Environment

/home/dgray24/clim_data3.yml

## References

ECMWF. (n.d.). ERA5. https://www.ecmwf.int/en/forecasts/datasets/reanalysis-datasets/era5

Climate Data Store. (2022). ERA5 Monthly Averaged Data on Single Levels from 1959 to Present. ECMWF & Copernicus Climate Change Service. 
https://cds.climate.copernicus.eu/cdsapp#!/dataset/reanalysis-era5-single-levels-monthly-means?tab=overview

Carroll, John. (2018). How the North Atlantic impacts Winter in Virginia. https://www.wfxrtv.com/digital-originals/how-the-north-atlantic-impacts-winter-in-virginia/

Hurrell, J.W., Kushnir, Y., Ottersen, G. and Visbeck, M. (2003). An Overview of the North Atlantic Oscillation. In The North Atlantic 
Oscillation: Climatic Significance and Environmental Impact (eds J.W. Hurrell, Y. Kushnir, G. Ottersen and M. Visbeck). https://doi.org/10.1029/134GM01
