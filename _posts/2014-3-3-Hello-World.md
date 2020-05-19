---
layout: post
title: You're up and running!
---

Next you can update your site name, avatar and other options using the _config.yml file in the root of your repository (shown below).

![_config.yml]({{ site.baseurl }}/images/config.png)

The easiest way to make your first post is to edit this one. Go into /_posts/ and update the Hello World markdown file. For more instructions head over to the [Jekyll Now repository](https://github.com/barryclark/jekyll-now) on GitHub.

## Introduction

`COVID-19`, popularly known as coronavirus is caused by a virus called SARS-CoV-2. It has caused irreparable damages world-wide to both economy and to public health. It is one of the deadliest pandemics of recent times that emerged in the last 2 decades. 

The main reason it caused so much of havoc is because of the long incubation time (~2 weeks) and the contagiousness of it. It transmits mainly through respiratory droplets produced when an infected person coughs or sneezes. These droplets can land in the mouths or noses of people who are nearby or possibly be inhaled into the lungs. Spread is more likely when people are in close contact with one another (within about 6 feet). 

United States is the worst affected country in the world with total number of cases at 14 M with more than 90 thousand deaths and counting. The need of this hour is to understand the most vulnerable section of the society and key levers to reduce the spread of COVID-19. It is equally important to learn from the policies that worked and keep improving the quality of healthcare at an increased pace. 

In this analysis, we looked at the publicly available county level data to generate insights that could help the spread of the disease. From our study, we have found that the most vulnerable section of the society are the old people especially who are above 65 years old. It also suggests that the densely populated areas with less per capita hospitals and doctors  are running a high risk of the spread within the county and also beyond it. Hence, based on our analysis we recommend social distancing and providing good health care in a timely manner to reduce the total number of deaths within counties.

## Literature Review

Curating a COVID-19 data repository and forecasting county-level death counts in the United States

The aforementioned talks about prediction techniques to estimate the total number of deaths due to covid-19 in the United States at county level using relevant data collected from various sources. The estimations are used to predict the deaths over a short-term period (e.g. Over the next week), and thus better understand the overall impact of the virus and accordingly implement social distancing policies. A weighted combination of 5 different exponential and linear predictive models were used for predicting the county level deaths.

We took inspiration from this paper to identify important features which the authors have used in their models. For eg, the paper explains how the total reported cases has little to no correlation with the total deaths, since high testing rate doesn’t necessarily imply high number of deaths.

```{r load-data, echo=FALSE, message=FALSE, warning=FALSE}
covid = read_csv(file = "data/county_data_apr22.csv")
```

## Data

The data is taken from a GitHub account with a large corpus of hospital-level and county-level data compiled from a variety of public sources to aid data science eforts to combat COVID-19. 

The team reponsible for this data is continually updating and adding to this repository. Currently, it includes data on COVID-19-related cases, deaths, demographics, health resource availability, health risk factors, social vulnerability, and other COVID-19-related information. 

For this analysis, we have used a small subset of the data set provided in the abridged version of the data due to various reasons like processing power.

## Unsupervised Learning

The main objective of the part is to understand the data in the context of the problem. For this analysis, we have chosen covariates based on a combination of technical and contextual understanding of the research question. 

The data come from all the major buckets defined in the GitHub account like geographical, demographics, and health-related risk and resource availability at a county level. Some of the variables seem more important than others like the _density of the county_, the _number of hospitals_, _ICU beds_ that are important factors during a pandemic like COVID-19. 
