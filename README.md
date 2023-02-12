# Personalized Relocation Helper README

Exploring Crime, Housing Prices, and Points of Interest (POI) )in 10 US States (California, Michigan, Texas, Colorado, North Carolina, Maine, Montana, Iowa, Oregon, Illinois)

## Overview

This project analyzes crime data, housing prices, and points of interest (POI) data for 10 US States of Interest. The crime data includes violent, non-violent, and total crime for each state in 2018-20022. The housing prices data includes the median housing price for each state from 2018-2022. The POI data provides the number of nearby Planetariums, Dog Friendly places, and Vegan Food for citiesi in each state. 

## Dependencies

* hvplot.pandas
* pandas
* requests
* json
* matplotlib.pyplot
* matplotlib.ticker
* geonamescache
* API Keys for Geoapify and FBI CDE must be included in a config.py file

## Date Resources

* Crime: [FBI CDE]([https://cde.ucr.cjis.gov/LATEST/webapp/#/pages/docApi](https://cde.ucr.cjis.gov/LATEST/webapp/#/pages/docApi))
* Housing: [Zillow Research Data ](https://www.zillow.com/research/data/)
* POI: [Geoapify](https://apidocs.geoapify.com/), [GeonamesCache](https://pypi.org/project/geonamescache/)

## Data

### Crime Data

The crime data was obtained from the FBI Crime Data Explorer API. The API was used to retrieve the number of violent and non-violent crimes for each state from 2018-2021. The data was then transformed to include a Total Crimes column and was pivoted to show the number of crimes for each state and year.

### Housing Prices

The housing prices data was obtained from the Zillow Research website. The CSV file includes the median housing price for each state from 2010-2022. Data from 2010-2017 was removed, and only data from 2018-2022 was kept. The StateName column was also removed, and the RegionName column was renamed to State. The data was then filtered to include only the ten selected states, and the State column was converted to state abbreviations.

### Points of Interest

The points of interest data includes three categories: Planetariums, Dog Friendly Places, and Vegan Food places. The Geonamescache library was used to obtain a list of cities and states in the United States. The list was then filtered to include only cities in the ten selected states. The latitude and longitude of each city were then used to query the Geoapify API for the number and names of nearby Planetariums, Dog Friendly Places, and Vegan Food places.

### Crime Data


## File Descriptions

* `exploring_housing_prices.ipynb`: The Jupyter Notebook that contains the code for the project
* `housing_prices_by_state.csv`: The CSV file that contains the housing prices data
* `config.py`: A Python file that contains the Geoapify and Crime API keys

## Usage

To use the project, simply run the `exploring_housing_prices.ipynb` notebook in a Jupyter Notebook environment. The notebook contains all the necessary code to analyze and visualize the data.
