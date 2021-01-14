# ETL_Project

## Table of Contents
* [Introduction](#introduction)
* [Extract](#extract)
* [Transform](#transform)
* [Load](#load)
* [Technologies](#technologies)

## Introduction
I wanted to look at if crude oil production has any impact on crude oil price and if there's any noticable impact on price of gasoline. This project will focus on only the United States and the crude oil price of WTI which is the benchmark price in the United States. 

## Steps Taken 
### Extract
I found all my data from the EIA (Energy Information Administration). Crude oil production and gasoline prices data were obtained in excel format. Crude oil price over the years was obtained via an API call.

### Transform
I had to clean up the column names and rename them to something shorter and reflect what was in the column. One of the datasets had the data in ascending order while the other two was in descending order, so I did a sort value to get it to match the other two. In addition to that, each dataset had a slightly different date range for the data, so I did a loc and identified the date range I want for all three datasets. After that I added a week number column so I can use that to visualize whether a week number had any impacts. I also did a merge of the crude oil datasets to show all crude oil information in one table.

### Load 
Finally everything was loaded into a SQL database with a total of two tables, one for crude oil and the other for gas prices. 

## Technologies
* Pandas
* API, JSON
* SQLAlchemy