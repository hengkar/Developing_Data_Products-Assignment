Data Analysis: Effect and Prediction of Automatic or Manual Transmission on Miles Per Gallon of cars
========================================================
author: Heng Kar
date: 28 Feb 2016

Overview
========================================================

This analysis is to explore the relationship between a set of variables on miles per gallon (MPG) (outcome). The analysis are particularly focus in the following two questions:

- "Is an automatic or manual transmission better for MPG"
- "Quantify the MPG difference between automatic and manual transmissions"


Exploring Data With Plot
========================================================

From plot, we can see some higher correlations between variables like 
- "hp"
- "wt"
- "am"

***

![plot of chunk unnamed-chunk-1](MotorTrendApplication-figure/unnamed-chunk-1-1.png)

Regression Analysis and Prediction
========================================================
The regression model will predict MPG based on, Transmission type, Weight and Horsepower. 

Linear regression model:


```r
fit <- lm(mpg ~ am + wt + hp, data = mtcars)
```

Coefficient:


|            |   Estimate| Std. Error|   t value| Pr(>&#124;t&#124;)|
|:-----------|----------:|----------:|---------:|------------------:|
|(Intercept) | 34.0028751|  2.6426593| 12.866916|          0.0000000|
|amManual    |  2.0837101|  1.3764202|  1.513862|          0.1412682|
|wt          | -2.8785754|  0.9049705| -3.180850|          0.0035740|
|hp          | -0.0374787|  0.0096054| -3.901830|          0.0005464|

Details of Application
========================================================

Shiny App Screen Shot
![Shiny App](MotorTrendApplication-figure/predict.png "prediction")

***

URL

- [Shiny Application](https://hengkar.shinyapps.io/MotorTrendAnalysis/)

- [GitHub Pitch Presentation](http://htmlpreview.github.io/?https://github.com/hengkar/Developing_Data_Products-Assignment/blob/master/MotorTrendApplication.html)

- [Rpub Pitch Presentation](http://rpubs.com/hengkar/156563)

- [GitHub Source Code](https://github.com/hengkar/Developing_Data_Products-Assignment)

