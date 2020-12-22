---
title: "Predicting Bikeshare Trip Generation"
date: 2019-04-13
published: true
tags: [Bikeshare, Philadelphia, Active Transportation]
categories: [Project]
excerpt: "Constructing Sci-kit Learn Machine Learning Model"
hv-loader:
	importance: "charts/importance.html"
toc: true
toc_sticky: true
---


## Fitting and Evaluating the Model

In this model, the training set and testing set has a 70%/30% split. After fitting a random forest model, a 5-fold cross-validation is conducted to optimize the hyperparameters.

```javascript
/# Evaluate the best random forest model/
best_random = grid.best_estimator_
grid.score(test_set, y_test)
```
> `0.40827975407227945`

The test score of the randomforest model is 0.41, which is not too satisfactory, but is much higher than the linear model test score, which is 0.14.

<div id="importance"></div>

The plot above shows that bikeshare system internal factors have significantly more important impacts on trip production than other factors.


## Prediction Result


Despite a low test score, this model generally gets a good grasp of the distribution of bikeshare trips in Center City and outside of Center City, but it doesn't capture the minute details which distinguish the performance of Indego stations within Center City. The model can potentially be improved given more precise demographic data. However, different people take bikeshare trips for various purposes, so it would be hard to predict trips based on a specific demographic trend. 


## Conclusion

A well-functioning bikeshare system plays an important role in promoting active transportation in cities. To build a robust bicycle network, bicycle infrastructure is crucial and will encourage citizens to use them. Currently Philadelphia's Indego stations are all in direct proximity to existent bike lanes, yet the bikeshare network still underserves a lot of Philadelphia neighborhoods. Therefore, the city has to further push forward programs and initiatives to invest on cycling infrastructure if it wants to establish a robust bicycle network.

![indego_photo](https://raw.githubusercontent.com/chelsang/MUSA550-final/master/assets/images/indego_photo.jpg)
*[Source](https://www.phillyvoice.com/indego-bike-share-philadelphia-rate-increase-spring-minimum-age/)*

