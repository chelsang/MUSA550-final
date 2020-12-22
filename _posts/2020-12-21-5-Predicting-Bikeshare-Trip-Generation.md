---
title: "Predicting Bikeshare Trip Generation"
date: 2019-04-13
published: true
tags: [dataviz, folium]
excerpt: "Constructing Sci-kit Learn Machine Learning Model"
hv-loader:
	IndegoStations: "charts/importance.html"
toc: true
toc_sticky: true
---


## Fitting the Model

In this model, the training set and testing set has a 70%/30% split. After fitting a random forest model, a 5-fold cross-validation is conducted to optimize the hyperparameters.

```javascript
/# Evaluate the best random forest model/
best_random = grid.best_estimator_
grid.score(test_set, y_test)
```
`0.40827975407227945`



<div id="importance"></div>

hv-loader:
	IndegoStations: "charts/IndegoStations.html"
![importance](https://raw.githubusercontent.com/chelsang/MUSA550-final/master/assets/images/correlation2.png)






This post will show examples of embedding interactive maps produced using [Folium](https://github.com/python-visualization/folium).

## OSMnx and Street Networks

The shortest route between the Art Museum and the Liberty Bell:

<div id="folium-chart-1"></div>

## Percentage of Households without Internet

<div id="folium-chart-2"></div>

See the [lecture 9B slides](https://musa-550-fall-2020.github.io/slides/lecture-9B.html) and the [lecture 10A slides](https://musa-550-fall-2020.github.io/slides/lecture-10A.html) for the code that produced these plots.






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
