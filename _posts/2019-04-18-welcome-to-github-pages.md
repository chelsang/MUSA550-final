---
title: "Introduction"
date: 2020-12-21T10:34:30-04:00
categories:
  - Project
tags:
  - Bikeshare
  - Philadelphia
  - Active Transportation
---

![Indego logo]({{ site.url }}{{ site.baseurl }}/assets/images/indego.png)

Indego bikeshare system is Philadelphia's official city-run bikeshare system. Initially launched in 2015, Indego currently has over 1,000 self-service bikes and 130+ stations across the city. 

This project will study how Indego bikeshare stations are connected to nearby facilities and run a model that simulates the bikeshare trip prediction process. Due to the scope of this project, the prediction might not be actual enough to derive new station implementation strategies but can act as a reference for policy decisions.

The data that supports this project mainly comes from [Indego Data Portal](https://www.rideindego.com/about/data/), [OpenDataPhilly](https://www.opendataphilly.org/) and [OpenStreetMap](https://www.openstreetmap.org/#map=4/38.01/-95.84).

In all, this project is divided into 4 parts:

* Temporal Spacial Distribution of Bikeshare Trips
	- Temporal Change Illustrated in a Datashader Map
* Exploratory Analysis of Indego Stations 
	- Distance from Nearby Facilities to Indego Stations
* Data Preparation for Prediction Model
	- Variable Selection and Correlation Testing
* Predicting Bikeshare Trip Generation
	- Constructing Sci-kit Learn Machine Learning Model


Please feel free to reach out should you have any questions about the methodology or data. Enjoy!



