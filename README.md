
# Module 4 -  Final Project Submission

## Introduction

In this project, I use SARIMA modeling on time series data to determine the best zip codes to invest in.


## The Deliverables

In this repo, you will find a Jupyter Notebook with all related code, a PDF of the presentation, and a recording of the business presentation wherein I explain all findings.

![](gif.gif)


## Objectives

* Given a raw data set, predict which zip codes will have the best rate of return over the next 5 years.


### The Project

I was provided with a data set of monthly average property values for properties in 14,723 zip codes in the US, with data starting as far back as April 1996 through April 2018. We were asked to select the 5 "best" zip codes to invest in after conducting time series analysis on the data.

I began with research to find US cities/towns that were experiencing growth during early 2018. A report from US News and World Report provided me with a list of 10 cities that were experiencing 2%+ growth between 2017 and 2018, a rate of growth much higher than national average.

Following that selection, I decided it would be best to remove any data on the markets pre January 2010. This was done to eliminate the noise that would otherwise be present in the data as caused by the market downturn in 2008-09. While there were some zip codes that showed a sluggish recovery and were exhibiting falling property values into 2010-11, the general trend of the 38 zip codes I examined was positive, linear growth.

Of the 38 zip codes, I selected 10 to model by determining which zip codes had the highest average year over year growth in property value from January 2010-April 2018.

I then conducted time series analysis using Seasonal Autoregressive Integrated Moving Average models. That involved generating stationary data, determining the order of the AR and MA portions of the model, and selecting an order of seasonality. All possible combinations were then iterated through to determine which model parameters provided the lowest AIC (goodness-of-fit) score. Those orders were then built into models and forecasts were made for pricing out to April 2023.

I then calculated the total predicted revenue of owning, renting, then selling the property after 5 years time and selected the 5 zip codes that would provide the best investment based on the return.


### Final Project Summary

Greeley, CO, Boise City, ID, and Redmond, OR were the three cities that contained the 5 zip codes I selected as being the best to invest in to maximize return on investment over the next 5 years. These zip codes met a number of criteria: they have growing populations, they had the highest average annual growth in property value during the time period of 2010-2018, and they had the highest projected return on investment on the property over the period of 2018-2023.
