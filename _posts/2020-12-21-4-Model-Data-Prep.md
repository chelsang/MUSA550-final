---
title: "Data Preparation for Prediction Model"
date: 2020-12-21
published: true
tags:[Bikeshare, Philadelphia, Active Transportation]
toc: true
toc_sticky: true
read_time: false
excerpt: "Variable Selection and Correlation Testing"
hv-loader:
	indego-station: "charts/IndegoStations.html"
---


## Where do bikeshare trips start?

To study trip generation, the following analysis will focus on the trio-starting stations. The map below shows that most trips start within Center City, and based on the previous analyses, they also "stay within" Center City. The most popular starting-stations are close to city center or Schuylkill River trail.

![start_dot](https://raw.githubusercontent.com/chelsang/MUSA550-final/master/assets/images/start_trip.png)

## Variable Selection

To run a trip prediction model, different types of variables and chosen, and they can be divided into the following categories:

**1. Bikeshare Internal Factors**
* Total number of docks at a given station _("totalDocks")_
* Distance to nearest Indego station _("logNearStationDists")_
* Demand (total starting trips) of the nearest 5 stations _("laggedTrips")_
<br>
**2. Facilities/Attractions nearby**
* Distance to restaurants, pubs, and bars _("logDistRests")_
* Distance to cafe _("logDistCaf")_
* Distance to parks _("logDistPk")_
* Distance to tourist attractions _("logDistTour")_
* Distance to supermarket _("logDistSupermkt")_ 
* (Binary) Located in Center City Business District or not _("within_centerCity")_ 
<br>
**3. Transportation Factors**
* Distance to subway stations _("logDistSubw")_
* Distance to bus stations _("logDistBus")_
* Distance to nearest intersection _("logIntersectionDists")_
<br>
**4. Population Statistics** (of the census block group where the station locates)
* Median Household Income _("medhhincome")_
* Percentage of Household Car Ownership _("percent_car")_


## Preliminary Correlation Test

![correlation](https://raw.githubusercontent.com/chelsang/MUSA550-final/master/assets/images/correlation.png)

A correlation test is conducted before running the machine learning model. According to the test, the variables that contribute the most to trip generation are:

* Effects of nearby Indego stations
	- Lagged trips
	- Distance to nearest Indego station
* Distance to subway
* Distance to cafe
* Distance to tourist attraction
<br>

Other factors, especially the demographic statistics, are not performing quite well in the test. It might be that Indego stations are clustered in Center City, and therefore the stations clusters will be assigned the same census data, so the model is unable to tell the nuanced difference between different stations.


## Updated Correlation Test

As a result, an updated correlation test is run to fix the 





This post will show examples of embedding interactive charts produced using [Altair](https://altair-viz.github.io) and [Hvplot](https://hvplot.pyviz.org/).

## Altair Example

Below is a chart of the incidence of measles since 1928 for the 50 US states.

<div id="altair-chart-1"></div>

This was produced using Altair and embedded in this static web page. Note that you can also display Python code on this page:

```python
import altair as alt
alt.renderers.enable('notebook')
```

## HvPlot Example

Lastly, the measles incidence produced using the HvPlot package:

<div id="hv-chart-1"></div>

## Notes

- See the [raw source code](https://raw.githubusercontent.com/MUSA-550-Fall-2020/github-pages-starter/master/_posts/2019-04-13-measles-charts.md) of this post for details on how these charts were embedded.
- See the [lecture 13A slides](https://github.com/MUSA-550-Fall-2020/week-13/blob/master/lecture-13A.ipynb) for the code that produced these plots.

**Important: When embedding charts, you will likely need to adjust the width/height of the charts before embedding them in the page so they fit nicely when embedded.**
