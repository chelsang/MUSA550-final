---
title: "Exploratory Analysis of Indego Stations"
date: 2020-12-21
published: true
tags:[Bikeshare, Philadelphia, Active Transportation]
excerpt: "Distance from Nearby Facilities to Indego Stations"
hv-loader:
  hv-chart-1: ["charts/IndegoStations.html", "500"]
toc: true
toc_sticky: true
---

<br>

## Indego Station Distribution

<div id="hv-chart-1"></div>

The above interactive map shows the distribution of all Indego bikeshare station in Philadelphia. By hovering over the stations, you can easily see the number of total docks available at each station and number of bikes available as of Dec 21, 2020 10:53AM. 

In general, the map shows that Indego has a relatively good coverage in Center City and its surrounding areas such as University City, Graduate Hospital, and Fairmount. Some stations can be found at the outlier of the city boundary, as those are lcoated near the Lincoln Financial Field, which is a football stadium near Navy Yard.

There is a lack of Indego station coverage in West Philly and particularly North Philly. The following maps will show the ease of access from designated facilities to the Indego bike stations.


## Mapping the Distance to Indego Stations

Below is a proposed selection of facilities that people frequently visit via cycling trips. Since cycling is a relatively "light" way of travel mode, the purpose of cycling trips can be diverse, such as leisure, sightseeing and commute. Therefore, the facilities chosen here can be categorized and form  3 groups that account for the different travel purpose of cyclers.

To interpret the maps, the general rule of thumb is that **the darker the color, the shorter the distance to reach a nearby Indego station from a given facility**.


### Cycle for Leisure

#### 1. Restaurants, Bars, and Pubs
![food_map](https://raw.githubusercontent.com/chelsang/MUSA550-final/master/assets/images/food.png)

Since locations of restaurants, bars, and pubcs are widely spread across the city, their ease of access pattern generally follows the distribution pattern of Indego stations. Particularly Indego has built a robust network in neighborhoods along the Delaware River Waterfront. 

#### 2. Cafe
![cafe_map](https://raw.githubusercontent.com/chelsang/MUSA550-final/master/assets/images/cafe.png)

Cafes are densely located in Center City and Fishtown area, so Indego stations are generally available for most of the cafes.

#### 3. Supermarket
![supermarket_map](https://raw.githubusercontent.com/chelsang/MUSA550-final/master/assets/images/supermarket.png)

To meet residents' needs, supermarkets are spread out similarly as restaurants. Supermarkets in West Philly have better access to Indego stations than the ones in North Philly.

#### 4. Parks
![park_map](https://raw.githubusercontent.com/chelsang/MUSA550-final/master/assets/images/park.png)

Parks outside of Center City generally lack access to Indego stations.

### Cycle for Sightseeing

#### 5. Tourist Attractions (Sightseeing Landmarks, Museums, Galleries)
![tour_map](https://raw.githubusercontent.com/chelsang/MUSA550-final/master/assets/images/tour.png)

Generally it is easy to get to tourist attractions through biking, as these attractions are mostly concentrated around Center City, where most of the Indego stations locate. 

### Cycle for Commute

#### 6. Subway Stations
![subway_map](https://raw.githubusercontent.com/chelsang/MUSA550-final/master/assets/images/subway.png)

The subway stations pictured in the map include **Market-Frankford Line** that operates from 69th Street Transportation Center (West Philly) to Frankford Transportation Center (NorthEast Philly) and **Broad Street Line** that connects South and North Philly. 

The terminal and close-to-terminal stations are lacking access to Indego services according to the map.

#### 7. SEPTA Bus Stations (Spring 2019 Stops by Route)
![bus_map](https://raw.githubusercontent.com/chelsang/MUSA550-final/master/assets/images/bus.png) <br>
Data acquired [here](https://septaopendata-septa.opendata.arcgis.com/datasets/spring-2019-stops-by-route). <br>

The SEPTA bus system has an extensive network across the city and covers the majority of Philadelphia's neighborhoods. However, the bikeshare system is not functioning well as a "last-mile" connector to the bus network due to the unease of immediate access.


## Section Conclusion

The Indego network is robust among most of the neighborhoods near downtown area but gradually becomes weak as it fades away from the city center. Although the demand to get to different facilities is not as strong in North Philadelphia as in Center City, residents in North Philadelphia might still be able to take advantage of bikeshare to get to nearby facilities if such access is provided.


