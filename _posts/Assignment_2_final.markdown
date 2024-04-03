---
layout: post
title:  "Assignment 2!"
date:   2024-04-03 10:09:02 +0200
categories: jekyll update
---

# How do police stations affect crimerates in the surrounding area?

## Introduction

Crime occurs throughout all of San Francisco, with some areas being more exposed to crime than others. The question is, does the presence of police stations have an effect on the rates of crime in the surrounding neighborhood and area?

## Preparing packages, importing data and formatting

The data used is supplied by DataSF which cover both the history of crime and the location of police stations. We will only be looking at crime data from 2011, as this aligns with the newest available data of police stations and coordinates.

## Police station coordinates

**Location data for each police station is used to do the calculations**

## Crime in vicinity

Now we will explore all of the police stations in San Fransico. As we will be looking at data present in a circular area around the police stations, it's important that the individual police station domains dont overlap and influence the data trends. This is mitigated by locating the pair of closest police stations.

**Calculating pair of closest police stations**

## Barcharts of crime occurrences and distance to police stations

The pair of closest police stations was found to be Southeren and Tenderloin station of 1.23km. As a result, a radius of interest around the police stations has been set to 500m.

The area around the police stations will be divided into rings. These will serve as bins for the barchart. To combat the inflation in the number of crime with the gradiually increasing ring area, a normalization will be done to represent a density of crime instead. This density is represented as crime pr. square meter and ensure a accurate comparison between the rings.

A function is created to iterate through the stations and search crime which is within the 500m boundary and sorted accordingly. Additionally, data is generated and stored to be used in both a Folium map and a Bokeh plot further in the analysis.

## Folium map after additional filters

## Comment

**Looking at the Barcharts** we see a slight increase in criminal activity moving away from the police stations, but also examples of the opposite as seen by Tenderloin station. As in the case of Richmond and Mission station, no distinct impact is observed. The area around the police station is generally more safe.

**Looking at the Folium map** we see can see gradient examples of both increases and decreases in crime around police stations. Taking Southeren station, a clear increase in crime density is seen, going from dark purple to yellow. The opposite can be seen by Tenderloin station. It's also apparent from the heatmap, that not alot of crime is done in parks, where the only noticeable ring by Park station is one aligning with a hotspot on Stanyan Street.

## Bokeh plot

A Bokeh plot is made covering the Ingleside police staition to investigate the different crime types and how the dominant type of crime change according to distance.

Upon inspection of the Bokeh plot and specially when playing around with the different crime types, especially *Assault, Vandalism* and *Larcency/Theft*, the reader will notice a significant spike from 350 - 500 meter from the police station. As for the crime most frequently commited close to the station we again see *Assault* and *Vandalism* accompanied by *Drug/Narcotics* with the nearest cases being just 125 meter away.

Notably, *driving under the influence* and *Weapon laws* are exclusively done away from the station.

## Conclusion

Modelling criminal behaviour around police stations using solely crime data can give a general picture of the current effect, but might not be the most nuanced tool to confirm or deny the explored query. Things such as increased police patrol and survailance, reporting bias, socioeconomic factors and known crime hotspots (as seen on Stanyan Street) might contribute to inflation of the numbers and thus the rings which have been analyzed.

For half of the police stations, safety increased closer to the police station, with the remaining stations either not having a change of crimerates or in the case of Tenderloin Station actually being more unsafe at close distance.

The approach for this analysis was influenced by the filters which were put in place to eliminate outliers around the police stations. Ontop, the limit of a 500m radius to not interfere with the data from other police stations narrowed down the scope. Further test could include looking at more remote police stations and broadening the area of investigation.
