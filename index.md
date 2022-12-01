# 30-Year Precipitation Analysis of Virginia
 
### Desmond Gray
#### CLIM 680 - Fall 2022

[Project Proposal](https://desmond-gray.github.io/clim680_project_proposal/)

## Introduction

My initial proposal was to comparie the difference between coarse GPCP precipitation data from stations and satellites with 
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

### Aggregates

![era5_agg1.png](https://desmond-gray.github.io/CLIM680-Project/era5_agg1.png)

![era5_agg2.png](https://desmond-gray.github.io/CLIM680-Project/era5_agg2.png)

### Anomalies



### NAO Composite

![era5_comp1.png](https://desmond-gray.github.io/CLIM680-Project/era5_comp1.png)

![era5_comp2.png](https://desmond-gray.github.io/CLIM680-Project/era5_comp2.png)

![era5_comp3.png](https://desmond-gray.github.io/CLIM680-Project/era5_comp3.png)

### [Function](https://desmond-gray.github.io/CLIM680-Project/ERA5_PythonFunction.ipynb)



### Linear Regression

![era5_linreg1.png](https://desmond-gray.github.io/CLIM680-Project/era5_linreg1.png)

## Results


## Summary



## Conda Environment

/home/dgray24/clim_data3.yml

## References

ECMWF. (n.d.). ERA5. https://www.ecmwf.int/en/forecasts/datasets/reanalysis-datasets/era5

Climate Data Store. (2022). ERA5 Monthly Averaged Data on Single Levels from 1959 to Present. ECMWF & Copernicus Climate Change Service. 
https://cds.climate.copernicus.eu/cdsapp#!/dataset/reanalysis-era5-single-levels-monthly-means?tab=overview

Carroll, John. (2018). How the North Atlantic impacts Winter in Virginia. https://www.wfxrtv.com/digital-originals/how-the-north-atlantic-impacts-winter-in-virginia/

Hurrell, J.W., Kushnir, Y., Ottersen, G. and Visbeck, M. (2003). An Overview of the North Atlantic Oscillation. In The North Atlantic 
Oscillation: Climatic Significance and Environmental Impact (eds J.W. Hurrell, Y. Kushnir, G. Ottersen and M. Visbeck). https://doi.org/10.1029/134GM01