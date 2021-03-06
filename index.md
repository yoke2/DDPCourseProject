---
title       : Developing Data Products Course Project
subtitle    : Google Maps Geocode Query Tool
author      : Yoke K. Wong
job         : Developing Data Products MOOC
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---


## Introduction

The Google Maps Geocode Query Tool aims to simplify the collection of geocodes by providing a simple interface for users to query latitude and longtitude coordinates.

The tool makes use of the Google Maps API service for latidue and longtitude coordnate information and the Shiny Package for User Interface creation.

--- .class #id 

## Advantages and Limitations

Advantages  
1. Users do not need to know Google Maps API and R.  
2. Latitude and Longtitude coordinates can be viewed and downloaded as CSV file.  
3. It's free! (Courtesy of Google Maps API)  

Limitations  
1. Only a maximum of 10 addresses can be queried at one time due to limits set for the free version of Google Maps API  


--- .class #id 

## Mechanism

The main function that queries Google Maps API for latitude and longtitude information is the `geoCode` function. This function takes in the search criteria and returns the latitude, longtitude, type of location and address identified.


```r
args(geoCode)
```

```
## function (address, verbose = FALSE) 
## NULL
```

```r
address <- geoCode("Johns Hopkins University, Baltimore");address
```

```
## [1] "39.329901"                                         
## [2] "-76.6205184"                                       
## [3] "APPROXIMATE"                                       
## [4] "Johns Hopkins University, Baltimore, MD 21218, USA"
```

--- .class #id 

## References

This Data Product is based on the code and guidance provided in the sources below.

1. https://gist.github.com/josecarlosgonz/6417633#file-googlemapsandr-md
2. http://www.r-bloggers.com/using-google-maps-api-and-r/



