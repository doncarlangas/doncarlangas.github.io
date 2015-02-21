---
title       : Predict time to travel 1/4 mile
subtitle    : A Coursera project
author      : Carlos Sanchez San Roman
job         : Consultant
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Index

1. Resume
2. Model
3. App usage


--- .class #id 

## Resume

This app is the final project of the Coursera Developing Data Prodcuts.

The goal of the app is to predict the expect time the user's car will take to travel 1/4 mile
starting from stop. 

Our prediction variables are car's horsepower and wight in pounds.

--- .class #id


## Model

To answer the question. I have fit a linear model on the mtcars data.

The linear model has to predictors  : hp and wt


The coefficients for hp and wt are


```r
 set.seed(3)
 fit <- lm(qsec ~ hp + wt, data=mtcars)
 fit$coefficients
```

```
## (Intercept)          hp          wt 
## 18.82558525 -0.02730962  0.94153237
```

--- .class #id

## App usage

The user has to move the sliders in order to select his car's horsepower and weight.

So the app can predict the expected time.


