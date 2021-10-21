# Traffic Data Analysis - Speed Camara in Action

## Introduction

Enforcement cameras operate throughout Australia monitoring all traffic passing their locations and detecting speed and red-light offences in real time. Each camera can monitor multiple lanes bi-directionally (towards and away from the camera). In managing detections of vehicles, each camera records the lane, speed and direction of every vehicle that passes by its location. Each camera logs the details of traffic in this way creating a data source for traffic volumes that can be analyzed to determine trends and identify anomalies.
One of the camera test locations is in Canterbury, Melbourne and the data for this project was provided from that camera. The speed limit in this zone is 60 kmph and camera covers three lanes:

1. Straight-on and left turn
2. Straight-on only and
3. Right turn only.

The daily traffic logs for two months formed the basis of this project, which the relevant data for each vehicle being:

- Date / time of detection
- Lane vehicle was travelling in
- Speed of the vehicle when observed.

The task involves:

- Data Cleaning
- Data Modelling
- Data Engineering
- Data Analysis

### Data cleaning using Python

1. Remove irrelevant data as the range date

### Data Modelling

Transformed the text files into csv file using Phython

### Data Engineering

- Importing pandas library to convert a CSV file into a dataframe
- Building a Dataframe
- Save outputs in a CSV
- Select limited number of columns from the existing dataframe and store it in a new dataframes

## Purpose of the project

The purpose of the project is two-fold:

1. Analyze the traffic data for patterns
2. Determine when most speeding offence occur for vehicles proceeding straight-on from the camera location
3. Identify speeding patterns
4. Use machine learning to predict:
   - Average speed for a lane and day of the week for specific times of day
   - Maximum speed for a lane and day of the week for specific times of day

## Approach

Reviewed the data that was provided by the camera owner to understand the content and volume. There were 500k+ observations logged. Of these some (typically when travelling less than 29km per hour indicated that the vehicle was coming to a stop (at traffic lights) or turning (left or right) and as such could be eliminated from the observations related to speeding at the site.

Wrote a python script to load all of the data from many log files into a Dataframe where upon it was needed to convert some data formats for date and time so that they could be processed easily.

Prepared the data for analysis using Tableau to create various charts and a dashboard, discovered patterns for speeding, including some surprising statistics on when this was most frequent and also at what times speeders were exceeding the limit by the greatest amounts.

After trying several machine learning models the polynomial algorithm had the higher accuracy to use to build a model using the traffic data to predict the two items of interest – average speed and maximum speed.
Having created the model, it was tested this with over 150k samples as well as some random manual test cases to compare with historic data.

When the model was satisfied with the accuracy then a python endpoint was created that deployed to a Tableau server using a TABPY client.

### Traffic Data Analysis using Tableau

![](https://github.com/malejandrasalgado/Speed-Camara-in-Action/blob/main/Images/Traffic%20Data%20Analysis.png)

### Machine Learning Demostration using Tableau

![](https://github.com/malejandrasalgado/Speed-Camara-in-Action/blob/main/Images/Machine%20Learning%20Demostration.JPG)
