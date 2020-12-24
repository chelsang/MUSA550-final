---
title: "4. Data Preparation for Prediction Model"
date: 2020-12-18
published: true
tags: [Bikeshare, Philadelphia, Active Transportation]
excerpt: "Variable Selection and Correlation Testing"
toc: true
toc_sticky: true

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

**2. Facilities/Attractions nearby**
* Distance to restaurants, pubs, and bars _("logDistRests")_
* Distance to cafe _("logDistCaf")_
* Distance to parks _("logDistPk")_
* Distance to tourist attractions _("logDistTour")_
* Distance to supermarket _("logDistSupermkt")_ 
* (Binary) Located in Center City Business District or not _("within_centerCity")_ 

**3. Transportation Factors**
* Distance to subway stations _("logDistSubw")_
* Distance to bus stations _("logDistBus")_
* Distance to nearest intersection _("logIntersectionDists")_

**4. Population Statistics** (of the census block group where the station locates)
* Median Household Income _("medhhincome")_
* Percentage of Household Car Ownership _("percent_car")_


## Preliminary Correlation Test

![correlation1](https://raw.githubusercontent.com/chelsang/MUSA550-final/master/assets/images/correlation1.png)

A correlation test is conducted before running the machine learning model. According to the test, the variables that contribute the most to trip generation are:

* Effects of nearby Indego stations
	- Lagged trips
	- Distance to nearest Indego station
* Distance to subway
* Distance to cafe
* Distance to tourist attraction

Other factors, especially the demographic statistics, are not performing quite well in the test. It might be that Indego stations are clustered in Center City, and therefore the stations clusters will be assigned the same census data, so the model is unable to tell the nuanced difference between different stations.

Noticeably, the factors that indicate distance to nearby facilities are highly correlated to one another, potentially due to [trip chaining](https://nhts.ornl.gov/2001/pub/tripchaining.pdf). Distance to bus stop and distance to supermarket is perfectly colinear. It might be that supermarket are easily accessible through bus network. 



## Updated Correlation Test

After taking off some variables that perform poorly in the correlation test, the updated list of variables include:

![correlation2](https://raw.githubusercontent.com/chelsang/MUSA550-final/master/assets/images/correlation2.png)

**1. Bikeshare Internal Factors**
* Total number of docks at a given station _("totalDocks")_
* Distance to nearest Indego station _("logNearStationDists")_
* Demand (total starting trips) of the nearest 5 stations _("laggedTrips")_

**2. Facilities/Attractions nearby**
* Distance to restaurants, pubs, and bars _("logDistRests")_
* Distance to cafe _("logDistCaf")_
* Distance to parks _("logDistPk")_
* Distance to tourist attractions _("logDistTour")_
* (Binary) Located in Center City Business District or not _("within_centerCity")_ 

**3. Transportation Factors**
* Distance to subway stations _("logDistSubw")_
* Distance to bus stations _("logDistBus")_


