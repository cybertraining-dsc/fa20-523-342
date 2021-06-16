---
date: 2021-03-15
title: COVID-19 Analysis
linkTitle: COVID-19
tags: ["project", "ai", "health"]
description: Comparison analysis between USA and China on number of new cases and new deaths and trying to find factors played big roles in this spread.
author: Hany Boles
resources:
- src: "**.{png,jpg}"
  title: "Image #:counter"
---

# COVID-19 Analysis

[![Check Report](https://github.com/cybertraining-dsc/fa20-523-342/workflows/Check%20Report/badge.svg)](https://github.com/cybertraining-dsc/fa20-523-342/actions)
[![Status](https://github.com/cybertraining-dsc/fa20-523-342/workflows/Status/badge.svg)](https://github.com/cybertraining-dsc/fa20-523-342/actions)
Status: final approved, Type: Project


Hany Boles, [fa20-523-342](https://github.com/cybertraining-dsc/fa20-523-342/), [Edit](https://github.com/cybertraining-dsc/fa20-523-342/blob/main/project/project.md)

{{% pageinfo %}}

## Abstract

By the end of 2019, healthcare across the world started to see a new type of Flu and they called it Coronavirus or Covid-19. This new type of Flu developed across the world and it appeared there is no one treatment could be used to treat it yet, scientists found different treatments that apply to different age ranges. In this project, We will try to work on comparison analysis between USA and China on number of new cases and new deaths and trying to find factors played big roles in this spread.
Contents

{{< table_of_contents >}}

{{% /pageinfo %}}

**Keywords:** Corona Virus, Covid 19, Health

## 1. Introduction

While the world is ready to start 2020 we heard about a new type of the Flu that it appears to be started in China and from there it went to the entire world. It appeared to affect all ages but its severity did depend on other factors that related to age, health conditions if the patient is a smoker or not?

This new disease attacked aggressively the respiratory system for the patient and then all the human body causing death. The recovery from this disease appeared to vary from area to area across the globe, Also the death percentage as well was and still vary from area to area. and then we decided to perform the analysis on weather temperature from one side and the covid 19 new cases and new death on the other side to see if the weather temperature plays a role or not with it.

## 2. Data-Sets

After observing many datasets [^1] [^2] [^3] to get a better understanding if there are common factors in the areas that have the larger number of new Covid 19 cases, we decided to proceed with the dataset provided by the World Health Organization [^1] because this dateset is being updated on a daily basis and has the most accurate data. Currently it appears that we are getting a second wave of coronavirus and so we will try to get the most recent data. We were able to use Webscraping to get the data we need from the World Health Organization website which is updated daily.

For the weather datasets, we looked at several datasets [^4] [^5] [^6] and we decided to use the data provided by visualcrossing website [^4]. This website helped us in getting the data we need which is daily average temperatures in the United States of America and China. We started to collect the data from 1/3/2020.

### 2.1 Preparing COVID 19 Data-Set

We started to work on Covid 19 dataset and we found that it is better to use webscraping to gather the dataset so every time we run the python script, we will get the most recent data and then we opened the CSV file and added it to a dataframe.

![Figure 1](https://github.com/cybertraining-dsc/fa20-523-342/raw/main/project/images/webscrap.jpg)

**Figure 1**: Downloading the Covid 19 dataset.

We then filtered only on United States of America so we can get all data belong to United States of America.

![Figure 2](https://github.com/cybertraining-dsc/fa20-523-342/raw/main/project/images/usa.jpg)

**Figure 2**: Capturing only USA data

Then we made 2 seperate graphs to depict the number of new cases and the number of new deaths in the USA throughout 2020 as shown below.

![Figure 3](https://github.com/cybertraining-dsc/fa20-523-342/raw/main/project/images/usa_new_cases_deaths1.jpg)

**Figure 3**: USA New Covid 19 cases and new deaths.

![Figure 4](https://github.com/cybertraining-dsc/fa20-523-342/raw/main/project/images/china.jpg)

**Figure 4**: Capturing China data.

We also made 2 seperate graphs to depict the number of new cases and the number of new deaths in China throughout 2020 as shown below.

![Figure 5](https://github.com/cybertraining-dsc/fa20-523-342/raw/main/project/images/china_new_cases_deaths.jpg)

**Figure 5**: China New Covid 19 cases and new deaths

### 2.2 preparing Weather Data-Set

For the weather temperature dataset, we cleaned all the un-needed data from the csv file we received from Visualcrossing website [^4], then we merged the temperature column with the csv file we prepared for the covid 19, so now we have one file per country that contains Date, Temperature, New cases, new deaths.


## 3. Methodology

We utilized the Indiana University system to process the collected data as it will need a strong system to process it. Also, we utilized Python, matplotlib for visualization purposes, and Jupyter notebook as programming software and platform.

## 4. Processing the Data

We started to process the final dataset we prepared and we examined the data for any correlation between the temperature and new cases for the United States of America and we found that there is no correlation there.

![Figure 6](https://github.com/cybertraining-dsc/fa20-523-342/raw/main/project/images/usa_new_dataset.jpg) 

**Figure 6**: USA Dataset after merging the data.

![Figure 7](https://github.com/cybertraining-dsc/fa20-523-342/raw/main/project/images/usacorr.jpg)

**Figure 7**: Correlation between the temperature and the new covid 19 cases for the United States of America.

Then we also processed the data for China and got the same results as the United States of America. We then looked at the analysis and in the case of the United States of America we found there is a correlation between the new covid cases and the current (cumulative) cases. On the contrary, for China we found no correlation between the new Covid cases and the current (cumulative) cases.

![Figure 8](https://github.com/cybertraining-dsc/fa20-523-342/raw/main/project/images/usacorrheat.jpg)

**Figure 8**: Heat map depicting the correlations between new cases, cumulative cases, new deaths, and cumulative deaths, respectively for the United States of America.

![Figure 9](https://github.com/cybertraining-dsc/fa20-523-342/raw/main/project/images/chinacorr.jpg)

**Figure 9**: Correlation between the new covid 19 cases and the current cases for China.

![Figure 10](https://github.com/cybertraining-dsc/fa20-523-342/raw/main/project/images/chinacorrheat.jpg)

**Figure 10**: Heat map depicting the correlations between new cases, cumulative cases, new deaths, and cumulative deaths, respectively for China.

We started to observe more data from another country so we chose the United Kingdom, and we found a correlation between the new covid 19 cases and the current (cumulative) cases.

![Figure 11](https://github.com/cybertraining-dsc/fa20-523-342/raw/main/project/images/uk_correlation.jpg)

**Figure 11**: Correlation between the new covid 19 cases and the current cases for the United Kingdom.

![Figure 12](https://github.com/cybertraining-dsc/fa20-523-342/raw/main/project/images/ukcorrheat.jpg)

**Figure 12**: Heat map depicting the correlations between new cases, cumulative cases, new deaths, and cumulative deaths, respectively for the United Kingdom.

## 5. Conclusion and Future Work	

After processing  all the data gathered in  search of a correlation between the weather, more specifically temperature, and the number of new cases in both China and the United States of America, the results clearly indicate  that the number of new cases and temperature are uncorrelated.  Nonetheless, the results suggest that there is a strong positive correlation (correlation coefficient > 0.8) between the number of new cases and the cumulative number of current cases in United states of America and United Kingdom. Hence, it appears that, in the absence of other mitigating factors, the number of the new cases will increase as long as the cumulative number of current cases keeps increasing.

While the new covid 19 cases and the current cases at China are uncorrelated, this might be due to false reporting or due to different factors are being used at China to reduce the number of the new cases.

Given the more recent developments pertaining to the discovery and distribution of vaccines it is suggested that the model be modified to include the number of vaccinations administered.  The objective in this case will be to discover any correlation between the number of new cases and both the number of the current cases as well as the number of vaccinations being given across at least the United Sates. Depending on the outcome it maybe possible to determine how effective the vaccines are and maybe predict, if possible, if ever the number of cases will diminish to zero.


## 6. Acknowledgements

The author would like to thank Dr. Geoffrey Fox, Dr. Gregor von Laszewski, and the associate instructors in the *FA20-BL-ENGR-E534-11530: Big Data Applications* course (offered in the Fall 2020 semester at Indiana University, Bloomington) for their assistance, suggestions, and aid provided during working on this project.

## 7. References

[^1]: Covid19.who.int. 2020. [online] Available at: <https://covid19.who.int/table> [Accessed 19 December 2020].

[^2]: Datatopics.worldbank.org. 2020. Understanding The Coronavirus (COVID-19) Pandemic Through Data | Universal Health Coverage Data | World Bank. [online] Available at: <http://datatopics.worldbank.org/universal-health-coverage/coronavirus/> [Accessed 19 December 2020].

[^3]: Kaggle.com. 2020. COVID-19 Open Research Dataset Challenge (CORD-19). [online] Available at: <https://www.kaggle.com/allen-institute-for-ai/CORD-19-research-challenge> [Accessed 19 December 2020].

[^4]: Visualcrossing.com. 2020. Weather Data Services | Visual Crossing. [online] Available at: <https://www.visualcrossing.com/weather/weather-data-services#/editDataDefinition> [Accessed 19 December 2020].

[^5]: The Weather Channel. 2020. National And Local Weather Radar, Daily Forecast, Hurricane And Information From The Weather Channel And Weather.Com. [online] Available at: <https://weather.com/> [Accessed 22 December 2020].

[^6]: Climate.gov. 2020. Dataset Gallery | NOAA Climate.Gov. [online] Available at: <https://www.climate.gov/maps-data/datasets/formats/csv/variables/precipitation> [Accessed 22 December 2020].
