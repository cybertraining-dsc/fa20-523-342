# COVID-19 Analysis

[![Check Report](https://github.com/cybertraining-dsc/fa20-523-342/workflows/Check%20Report/badge.svg)](https://github.com/cybertraining-dsc/fa20-523-342/actions)
[![Status](https://github.com/cybertraining-dsc/fa20-523-342/workflows/Status/badge.svg)](https://github.com/cybertraining-dsc/fa20-523-342/actions)
Status: in progress approved, Type: Project


- [x] pease review margkown which does not have hanging indent
- [x] urls are in <http://www.google.com>
- [x] add refs as footnotes
- [x] Please use references instead of URLs. 
- [x] Reach office hours if help is needed
- [x]  please review our template to see how to do references and cite them in the text

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

This new disease attacked aggressively the respiratory system for the patient and then all the human body causing death. The recovery from this disease appeared to vary from area to area across the globe, Also the death percentage as well was and still vary from area to area. and then we decided to do some analysis to see if the weather temperature plays a role or not with it.

## 2. Data-Sets

After observing many datasets [^1], [^2], [^3] so we can get a better understanding if there is a common one or more factors in areas that have most number of Covid 19 new cases  between, We have decided to proceed using the data set provided by the World Health Organization [^1] because this dateset is being updated on daily basis and have the most accurate data. Currently looks like we are getting a second wave of coronavirus and so we will try to get the most recent data. We were able to use Webspraping to get the data we need from the World Health Organization website which is updated daily.

For the weather datasets, we looked at several datasets [^4], [^5], [^6] and we decided to use the data provided by visualcrossing website [^4]. This website helped us on getting the data we need which daily average temperatures at United States of America and China so we can use it for this project.
We started to collect the data from 1/1/2020.

### 2.1 preparing COVID 19 Data-Set

We started to work on Covid 19 dataset and we found that it is better to use webscraping to gather the dataset so every time we run the python script, we will get the most recent data and then we opened the CSV file and added it to a dataframe.
![Figure 1](https://github.com/cybertraining-dsc/fa20-523-342/blob/main/project/images/Webscrap.jpg)

**Figure 1**: Downloading the Covid 19 dataset.

We then filtered only on United States of America so we can get all data belong to United States of America

![Figure 2](https://raw.githubusercontent.com.com/cybertraining-dsc/fa20-523-342/blob/main/project/images/USA.jpg)
**Figure 2**: Capturing only USA data

Then we made a graph between the new cases and new deaths for USA

![Figure 3](https://github.com/cybertraining-dsc/fa20-523-342/blob/main/project/images/USA_NEW_Cases_Deaths1.jpg)
**Figure 3**: New cases and new deaths


raw.githubusercontent.com

While this was very helpful method to get the latest data, we couldn't use it to gather theweather dataset, we gathered the weather dataset by downloading from the Visualcrossing website [^4] 
------> processing data ----- to be moved
We will collect the data and extract it from its sources and datasets, Also we will look for the most recent data as well, and we will compare and do analysis on the findings and draw the most apropriate conclusion accordingly.


## 3. Methodology

We will be utilizing the Indiana University system to process the collected data as it will need a strong system to process it. Also, we will utilize Python, and Jupyter notebook as programming software and platform.
After observing the data from multiple websites, we decided to use the dataset from the World Health Organization. After looking through the data we decided to perform the analysis between the USA and China on the total number of new COVID 19 cases and total number of new COVID 19 related deaths on a monthly basis starting from January 2020.
We started with using Python code for the programing and working on the csv file downloaded from the WHO website, and utilizing matplotlib for visualization purposes. 

## 4. Conclusion and Future Work	

After processing  all the data gathered in  search of a correlation between the weather, more specifically  temperature, and the number of new cases in both China and the United States of America, the results clearly indicate  that the number of new cases and temperature are uncorrelated.  Nonetheless, the results suggest that there is a strong positive correlation (correlation coefficient > 0.8) between the number of new cases and the cumulative number of current cases in both countries. Hence, it appears that, in the absence of other mitigating factors, the number of the new cases will increase as long as the cumulative number of current cases keeps increasing.

Given the more recent developments pertaining to the discovery and distribution of vaccines it is suggested that the model be modified to include the number of vaccinations administered.  The objective in this case will be to discover any correlation between the number of new cases and both the number of the current cases as well as the number of vaccinations being given across at least the United Sates. Depending on the outcome it maybe possible to determine how effective the vaccines are and maybe predict, if possible, if ever the number of cases will diminish to zero. 


## 5. References

[^1]: Covid19.who.int. 2020. [online] Available at: <https://covid19.who.int/table> [Accessed 19 December 2020].

[^2]: Datatopics.worldbank.org. 2020. Understanding The Coronavirus (COVID-19) Pandemic Through Data | Universal Health Coverage Data | World Bank. [online] Available at: <http://datatopics.worldbank.org/universal-health-coverage/coronavirus/> [Accessed 19 December 2020].

[^3]: Kaggle.com. 2020. COVID-19 Open Research Dataset Challenge (CORD-19). [online] Available at: <https://www.kaggle.com/allen-institute-for-ai/CORD-19-research-challenge> [Accessed 19 December 2020].

[^4]: Visualcrossing.com. 2020. Weather Data Services | Visual Crossing. [online] Available at: <https://www.visualcrossing.com/weather/weather-data-services#/editDataDefinition> [Accessed 19 December 2020].

[^5]: The Weather Channel. 2020. National And Local Weather Radar, Daily Forecast, Hurricane And Information From The Weather Channel And Weather.Com. [online] Available at: <https://weather.com/> [Accessed 22 December 2020].

[^6]: Climate.gov. 2020. Dataset Gallery | NOAA Climate.Gov. [online] Available at: <https://www.climate.gov/maps-data/datasets/formats/csv/variables/precipitation> [Accessed 22 December 2020].
