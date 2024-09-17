---
layout: page
title: Model Methodology
icon: fa-calculator
order: 2
level: 1
excerpt_separator: <!--more-->
moretext: more methodology
---

*[This methodology section is a work in progress. Please check back for a more complete version.]*

The underlying code for the charts and models in the COVID-19 section of this website are available on my [github page](https://github.com/donnellymjd/coronita).

<h3>Reproduction Rate Model</h3>
The code used to estimate the time-varying reproduction rate leverages several available data sources that could imply the true reproduction rate. Specifically, the model uses daily deaths, hospital admissions, concurrent hospitlizations, daily cases, and test positivity rate. Outliers in the raw data are removed. Each of these data are lagged by a relevant period of time, based on an average number of days for the represented event to occur. These time periods are represented on the charts. After lagging the data, the model uses a weighted average of the daily percent change in each series. 

<h3>Forecasting Model</h3>
The core forecasting model is based on the standard SEIR epidemiological model, with one major modification. This model uses daily cohort groups. One new cohort is kicked off for each day's new set of COVID-19 exposures. This cohort-based approach ensures that policy changes that effect the reproduction factors for future days do not impact the forecasts for new hospitalizations and deaths of individuals already infected, as can be the case in the classic compartmental SEIR model. 

