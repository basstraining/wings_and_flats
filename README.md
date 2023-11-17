![Airbus320](https://upload.wikimedia.org/wikipedia/commons/c/c1/Airbus_A320-214%2C_Airbus_Industrie_JP7617615.jpg)

# Aircraft Safety Analysis

## Overview
Our analysis aims to disinter meaningful insights from the dataset accessed from Kaggle as it relates to aviation accidents. This data contains the necessary information to develop our supporting arguments to form three concrete business recommendations: assessing the overall safety of planes, charting less treacherous skies, and focusing on commercial flights. With the cumulative knowledge we have fostered as budding data scientists, we aim to take you through cleaning, analyzing, and visualizing this aviation accident data. We hope the insight we provide can provide the basis for actionable results.

## Business Understanding
The overall purpose of conducting this analysis is to provide the safest customer experience possible while streamlining our resources to maximize profits. To do this, we must determine the parameters necessary to assess these considerations. Questions to be considered are: What determining factors will be used to evaluate the safety of the planes we want to acquire? What travel routes are the safest, and what are more profitable, commercial or private airlines? These questions help to provide the framework for our analysis, which we will delve into in the sections below.

## Data Understanding
This data we worked with comes from the National Transportation Safety Board, which includes aviation accident data from 1962 to 2023 about civil aviation accidents and selected incidents in the United States and international waters. Among all the columns in our data set, we set some crucial to our analysis: the goal is to determine which aircraft is the safest model to use.
Along the process, we used these columns for our analysis, which included the following variables:
 -- Event ID
 -- Total fatal injuries, total serious injuries, total minor injuries, total uninjured;
 -- Make and model
 -- Location, latitude, and longitude

This data contains critical information to needed understand the accidents' severity and which make/model had the worst accident records.

## Data Preparation (Can be really short in README)
To adequately prepare our data, we cleaned it up by filtering out the nulls, reorganizing and grouping the make and model data as our subsets, and dropping the columns that did not provide helpful information or had many missing values. We also extracted data from external resources to supplement our study. We recognized it would be beneficial to include data that spoke to the annual total deliveries of the make/model from aircraft manufacturing companies, and we also added a geographical map helping us pinpoint accident locations. 

## Analysis and Results/Recommendations
To analyze the data, we developed a formula: Severity score.
This score indicates the gravity and impact of a crash based on the count of injured people normalized by total passengers:
nv1 = DF[uninjured]
nv2 = DF[minor injuries]
nv3  = DF[severe injuries]
nv4 = DF[fatal injuries]
Severity Score = (nv1+(3*nv2)+(12*nv3)+(25*nv4))/People Count

## Conlusion and Next Steps
Our analysis aims to find the safest make/model using the National Transportation Safety Board data and determine which regions will be the least risky for routes. After some data cleaning, with the help of a formula that we generated and some external resources, we were able to give out the recommendations: Airbus 320 is the safest model for international travel (targeting Japan, Europe, and South America especially) and ATR 72 is the best option (safety wise) for regional trips (targeting coastal areas in the US). The following steps will be finding and comparing the prices and maintenance costs of the models that we suggested and doing more marketing research on the regions that we recommended; by doing that, we should be able to come up with a better idea of how we can make this new business profitable at the lowest risk.

## Repo Structure
|---data

|---images

|---notebooks

|--Aviation_Analytics__Risk_Management_2.pdf

|---final.ipynb
