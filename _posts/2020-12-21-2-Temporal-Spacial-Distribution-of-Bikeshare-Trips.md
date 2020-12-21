---
title: "Temporal Spacial Distribution of Bikeshare Trips"
date: 2020-12-21
published: true
tags:[Bikeshare, Philadelphia, Active Transportation]
toc: true
toc_sticky: true
read_time: false
excerpt: "Temporal Change Illustrated in a Datashader Map"
hv-loader:
	indego-station: "charts/IndegoStations.html"
---

<br>

## Indego Trip Distribution

<div id="indego-station"></div>

The above interactive map shows the distribution of all Indego bikeshare station in Philadelphia. By hovering over the stations, you can easily see the number of total docks available at each station and number of bikes available as of Dec 21, 2020 10:53AM. 

In general, the map shows that Indego has a relatively good coverage in Center City and its surrounding areas such as University City, Graduate Hospital, and Fairmount. Some stations can be found at the outlier of the city boundary, as those are lcoated near the Lincoln Financial Field, which is a football stadium near Navy Yard.

There is a lack of Indego station coverage in West Philly and particularly North Philly. The following maps will show the ease of access from designated facilities to the Indego bike stations.


## Mapping the Distance to Indego Stations

### 1. Restaurants, Bars, and Pubs

Below, we show the distance between residential sales and the average distance to the 5 nearest 311 calls for abandoned cars.

![distances-abandoned-cars]({{ site.url }}{{ site.baseurl }}/assets/images/distance_to_abandoned_cars.png)
