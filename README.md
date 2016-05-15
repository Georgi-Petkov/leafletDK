
<!-- README.md is generated from README.Rmd. Please edit that file -->
leafletDK is a package that makes it easy to create interactive dynamic leaflet maps based on danish administrative areas

The package is heavily inspired by the amazing mapDK package by Sebastian Barfort, which I recommend if you want to create static high quality maps.

Getting started
---------------

It is really easy to use leafletDK. Simply call the administrative area that you want to map (like a municipality) and give it the data you want the map to be colored by.

Below is an example where we load data from Statistics Denmark and map it using leaflet.

    library(leafletDK)

    folk1 <- read.csv2("http://api.statbank.dk/v1/data/folk1/CSV?OMR%C3%85DE=*",
                       stringsAsFactors = F)

    municipalityDK("INDHOLD", "OMRÅDE", data = folk1)

    municipalityDK("INDHOLD", "OMRÅDE", subplot = c("frederiksberg","hvidovre"), data = folk1)