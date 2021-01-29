# Surfs_up
Weather analysis using SQLite and SQLAlchemy. Climate App building using Flask. Other tools include Python and Jupyter Notebooks.
## Overview of Surfs Up Analysis

The purpose of this analysis is to review a dataset pertaining to weather conditions that has been stored in a [SQLite database](https://github.com/amylio/Surfs_up/blob/main/MOD9_Challenge_Submission/hawaii.sqlite) to provide information that will convince an investor that opening up a **Surf n' Shake** shop in Oahu, Hawaii is a good business idea. The idea is that the shop will sell surf boards and ice cream throughout the year, but the investor is hesitant because he invested in a similar business that failed due to the weather conditions. In order to get this investor on board, we need to provide statistical analysis specifically on the weather conditions in Oahu that will convince him that this will be a successful business venture.

In order to explore the data in the `SQLite` database, we used `SQLAlchemy` to connect and generate queries to pull the necessary information needed for our analysis. Throughout this module, we used [Jupiter notebook](https://github.com/amylio/Surfs_up/blob/main/climate_analysis.ipynb) to import dependencies and create the commands to pull the data from the `SQLite` database. Some of the features/functions that we learned in this module included:

**SQLAlchemy**
* `ORM` (Object Relational Mapper)
* Differences between a **decoupled system** and a **tightly coupled system**
* `Create Engine` function
* `Automap Base` function
* **Reflect Tables** using `prepare` function
* `Session` link to database

Below is a sample of the dependencies and functions that were used to access the content in the `SQLite` database:

![SQLAlchemy](https://github.com/amylio/Surfs_up/blob/main/MOD9_Challenge_Submission/Images/SQLAlchemySample.png)

We also used `Visual Studio Code` to create Python applications to share the results via a webpage by creating `Flask` routes and using Terminal to run the `Flask` app. When running the `Flask` app in `Terminal`, it generated the `Flask` routes in a web address `http://127.0.0.1:5000` that could be shared.

![flask](https://github.com/amylio/Surfs_up/blob/main/MOD9_Challenge_Submission/Images/FlaskRoute.png)
![terminal](https://github.com/amylio/Surfs_up/blob/main/MOD9_Challenge_Submission/Images/TerminalImage.png)
![web](https://github.com/amylio/Surfs_up/blob/main/MOD9_Challenge_Submission/Images/FlaskWebpage.png)

## Results

When we pulled the data, we first looked at the the precipitation for a one year timeframe. We reviewed the activity from August 23, 2016 - August 23, 2017. The average was 18% based on 2,021 observations. This tells us that throughout the year, Oahu was mostly sunny throughout the day and experienced low rainfall. 

![precipstats](https://github.com/amylio/Surfs_up/blob/main/MOD9_Challenge_Submission/Images/PrecipStats.png) 
![precipgraph](https://github.com/amylio/Surfs_up/blob/main/MOD9_Challenge_Submission/Images/PrecipGraph.png)

We also looked at the number of weather stations that were actively collecting precipitation data and focus on one station that had the most observations recorded. In total, there were (9) stations with `USC00519281` showing the highest amount of observations at 2,772 entries. We used the information from this station to review the temperature for the same time period. The results showed that the average temperature throughout the year was **72°F** with a low of **54°F** and a high of **85°F**. 

![tempgraph](https://github.com/amylio/Surfs_up/blob/main/MOD9_Challenge_Submission/Images/tempgraph.png)

We then expanded our results to look at all of the observations that were recorded in the month of **June** and **December** regardless of year, the results showed:

* The average temperature is in the 70's.
* Both June and December showed similar min/max and average temperatures.
* The assumption is that the temperature does not have dramatic fluctuations throughout the year.

![June](https://github.com/amylio/Surfs_up/blob/main/MOD9_Challenge_Submission/Images/JuneStats.png)  ![Dec](https://github.com/amylio/Surfs_up/blob/main/MOD9_Challenge_Submission/Images/DecStats.png)

## Summary

In summary, the temperature in Oahu is relatively the same throughout the year and the chances of continuous rainfall is low. When we rewrite the queries to add precipitation to the results for June and December, the average precipitation in those months showed:

* June at 14%
* December at 22%

![junepre](https://github.com/amylio/Surfs_up/blob/main/MOD9_Challenge_Submission/Images/JunePrecip.png)  ![decpre](https://github.com/amylio/Surfs_up/blob/main/MOD9_Challenge_Submission/Images/DecPrecip.png)

Looking at the precipitation and the temperature proves that investing in **Surf n' Shake** is a good business venture and that Oahu, Hawaii is the ideal location.

### Bonus Information

If we looked at the same datapoints for March and September to give us a more robust look at the weather conditions in this location, the results tell us that the chances of rain is higher in the Winter months (Dec-Mar), but the temperature averages to be the same. Therefore, this further supports that **Surf n' Shake** will be successful business at this location.

![Mar](https://github.com/amylio/Surfs_up/blob/main/MOD9_Challenge_Submission/Images/MarStats.png). ![Sept](https://github.com/amylio/Surfs_up/blob/main/MOD9_Challenge_Submission/Images/SeptStats.png)
