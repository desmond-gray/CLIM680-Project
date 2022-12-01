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

The datasets used in my project is The [ERA5 Global Reanalysis](https://www.ecmwf.int/en/forecasts/datasets/reanalysis-datasets/era5) provides hourly estimates of a large number 
of atmospheric, land, and oceanic climate variables from Jan 1959 to present.  It is on a 30km grid. ERA5 combines vast amounts of historical 
observations into global estimates using advanced modelling and data assimilation systems. Because of the size of this data set, I will only be
working with the state of Virginia, while focusing on the variable of total precipitation (mtpr) between the years of 1980-2009. I chose the latitude 
and longitude ranges of 84W to 74W and 36N to 40N.

## Code Description

### GroupBy

### Aggregates

### Anomalies

### NAO Copmosite

### Linear Regression

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
