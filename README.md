# Personalized Relocation Helper README

#### Task List

Alejandra (Before Class):

* [ ] Crime per capita dataframe - make sense of what values need to go in there
* [ ] Subplot for horizontal stacked bar graphs
* [ ] Summary of Crime findings
* [ ] Presentation Slide Deck

Lisa (Before Class):

* [ ] POI per capita - make sense of values
* [ ] Vizualize POI per capita
* [ ] Summary of housing findings
* [ ] Summary of POI findings

Monday Class/After

* [ ] Crime and Housing Visualization
* [ ] Housing and POI Visualization
* [ ] Summary of Comparative Visualizations
* [ ] Save jpgs of visualizations
* [ ] Maybe screen grab relevant code
* [ ] Rehearse presentation

**Things needing to be addressed:**

* [ ] *Crime Visualization - subplotting horizontal stacked bar graph for each year
* [ ] Summary of Crime Visualization
* [X] *Housing Visualization - multiple line graph comparing states
* [ ] Summary of Housing Visualization
* [X] *POI Visualization - POI by Cities in States map
* [X] *POI Visualization - POI by States map
* [ ] *POI Visualization - POI per capita
* [ ] Summary of POI Visualization
* [ ] *Comparing Crime and Housing Visualization
* [ ] *Comparing Housing and POI Visualization
* [ ] Summary of Comparative Visualizations

**Things needing to be addressed:**

* [ ] Crime needs to be adjusted per capita. When this is done, a note needs to be made above in the Crime Data section and then per capita also needs to be noted in the Crime Visualization section
* [ ] Would like to ensure that the median is accurately captured, but for now we'll assume it is accurate.
* [ ] Would like to remove duplicates in the POI. If unable to do so, a note may need to be made in the above sections and in the limitations section that the coumt for each POI is contingent the count per city and may not accurately represent the count per state.

#### Presentation (7min, 3min for QnA)

* [ ] An executive summary or overview of the project and project goals:

* Project Description/Outline: We're in the relocation business. We already have a solid method for moving people here, there, and everywhere, but business is slow. After doing some market research, we learned that there are lots of people out there who would like to move, but are having trouble finding where to move. That's where the Personalized Relocation Helper (PRH) come in! While we're in the beginning stages of developing the PRH in the hopes of marketing it as a free tool that will hopefully generate business!
* The presentation you are about to see hopes to give us some insight into the three categories people often consider when moving: Crime, Housing Price, and the Coolness (not in terms of weather, but in terms of having cool places to go!).
* We're using a sample of 10 states (States of Interst: California, Michigan, Texas, Colorado, North Carolina, Maine, Montana, Iowa, Oregon, and Illinois). We'll look at the crime data for each of these states, categorized by violent and non-violent. We'll look at the median housing price, and then we'll look at points of interest. For the purposes of this initial launch, we've narrowed down points of interest a bit further to include places within 5 miles of a city (pop 15000+) in one of the States of Interest. Our goal is to help our demo client visualize and understand the data collected collected data to help them in selecting a state.

* [ ] An overview of the data collection, cleanup, and exploration processes:Describe the source of your data and why you chose it for your project.

* Describe the collection, exploration, and cleanup process.

* [ ] The approach that your group took to achieve the project goals:

* Include any relevant code or demonstrations of the application or analysis.
* Discuss any unanticipated insights or problems that arose and how you resolved them.

* [ ] The results/conclusions of the application or analysis:

* Include relevant images or examples to support your work.
* If the project goal was not achieved, discuss the issues and how you attempted to resolve them.

* [ ] Next steps: Briefly discuss potential next steps for the project.

#### Requirements Check

* [ ] Completed Analysis Uploaded to GitHub (20 points)

* Final data analysis contains ample and complete information in README file (10 points)
* Final repository is acceptable for professional quality presentation (10 points)

* [ ] Visualizations (20 points)

* sub
* 6–8 visualizations of data (at least two per question) (10 points)
* Clear and accurate labeling of images (5 points)
* Visualizations supported with ample and precise explanation (5 points)

* [ ] Analysis and Conclusion (20 points)

* Write-up summarizes major findings and implications at a professional level (5 points)
* Each question in the project proposal is answered with precise descriptions and findings (5 points)
* Findings are strongly supported with numbers and visualizations (5 points)
* Each question response is supported with a well-discerned statistical analysis from lessons (e.g., aggregation, correlation, comparison, summary statistics, sentiment analysis, and time series analysis) (5 points)

* [ ] Group Presentation (20 points)

* All group members spoke during the presentation (5 points)
* Group was well prepared (5 points)
* Presentation is relevant to material (5 points)
* Presentation maintains audience interest (5 points)

* [ ] Slide Deck (20 points)

* Slides are visually clean and professional (5 points)
* Slides are relevant to material (5 points)
* Slides effectively demonstrate the project (5 points
* Slides are clear and maintain audience interest (5 points)

## REMOVE THIS LINE AND EVERYTHING ABOVE BEFORE SUBMISSION

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

## Data

### Crime Data

The crime data is collected using the [FBI Crime Data Explorer API]([https://cde.ucr.cjis.gov/LATEST/webapp/#/pages/docApi](https://cde.ucr.cjis.gov/LATEST/webapp/#/pages/docApi)). The API retrieved data on several types of crime *where a charge was made* in each state from 2018-2021. The types of crime were then sorted to violent and non-violent* crimes and then totaled. This was then pivoted to more clearly display the data.

*Note: While violent and non-violent crimes both have significant consequences to individuals and communities, violent crimes are considered more serious due to the physical harm caused, and therefore separate.

* Violent crime includes four offenses: Murder and Non-negligent 			 	Manslaughter, Rape, Robbery, and Aggravated Assault.
* Non-violent crime includes All Other Offenses (Except Traffic), Arson, Burglary, Curfew and Loitering Law Violations, Disorderly Conduct, Driving Under the Influence, Drug Abuse Violations - Grand Total, Drunkenness,
  Embezzlement, Forgery and Counterfeiting, Fraud, Gambling - Total, Human
  Trafficking - Commercial Sex Acts, Human Trafficking - Involuntary
  Servitude, Larceny - Theft, Liquor Laws, Manslaughter by Negligence,
  Motor Vehicle Theft, Offenses Against the Family and Children,
  Prostitution and Commercialized Vice, Stolen Property: Buying,
  Receiving, Possessing, Suspicion, Vagrancy, Vandalism, Weapons:
  Carrying, Possessing, Etc., Sex Offenses (Except Rape, and Prostitution
  and Commercialized Vice), Simple Assault.

### Housing Prices

The housing price data is collected from a csv file on the [Zillow Research Data](https://www.zillow.com/research/data/) website. The data was narrowed to only include 2018-2022 data for the 10 states of interest. Interpolate was used to get the average of adjacent cells in a State row when there was an absent value. The median house price for each year by state was then calculated.

### Points of Interest

Using [GeonamesCache](https://pypi.org/project/geonamescache/), a list of cities (pop. >15000) in each of the states of interest generates. Then, [Geoapify](https://apidocs.geoapify.com/) searches for Planetariums, places where dogs are allowed, and places where you can get vegan food within a 5 mile radius of each city. These three variables were selected based on the idea of a demo client wanting to further narrow down their search for a place to relocate.

## Visualizations

### Visualizing Violent, Non-Violent, and Total Crime in States of Interest

The crime data is visualized using subplot to display a horizontal bar chart referencing the violent, non-violent, and total crimes per state for the 2018-2021 timeframe. ****This shows that...*

### Visualizing Median Housing Prices in States of Interest

The housing price data is visualized using a multiple line graph to display the median house prices per state for the 2018-2022 timeframe. ****This shows that...*

### Visualizing Points of Interest in States of Interest

The points of interest data is displayed by using two maps and ****visualization_type.* The first map visualizes the number of POIs for each city in the states of interest. The second map visualizes the number of POIs for each state. The ****visualization_type* helps visualize the POIs taking the population in to consideration. ****This shows that...*

### Visualizing How Crime and Housing Prices Compare

The crime data and housing price data are compared by displaying the data in ****visualization_type.* ****This shows that...*

### Visualizing Points of Interest and Housing Prices Compare

The crime data and housing price data are compared by displaying the data in ****visualization_type. ***This shows that...*

## Limitations

* Ideally, this project would have included the ability to more easily make selections for states of interest and points of interest to broaden its usefullness.
* Current crime data is limited by state and is unavailable to be pulled by city without proper authorization. This limits the ability to zoom in on additional comparisons that could have otherwise been made.
* As noted, the crime data includes crime where a charge was made. This does not include reported crimes or undocumented crimes.
