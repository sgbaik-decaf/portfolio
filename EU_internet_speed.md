# Internet speed of European Countries

Click blue "portfolio" to return to main.

There is an interactive map embedded in it. Wait till it loads. If prompted, log in with your CMU or ESRI account.

For iPad users: a fullscreen alternative is available [here](https://carnegiemellon.maps.arcgis.com/apps/instant/sidebar/index.html?appid=0781e9e4284c41248d0303d50ab5ee02)

<iframe src="https://carnegiemellon.maps.arcgis.com/apps/instant/sidebar/index.html?appid=0781e9e4284c41248d0303d50ab5ee02" width="1200" height="800" frameborder="0" style="border:0" allowfullscreen>iFrames are not supported on this page.</iframe>

## ORIGINAL VISUALIZATION

Average internet speed across Europe

Ornaldo Gjergji, European Data Journalism Network

[europeandatajournalism.eu](https://datavis.europeandatajournalism.eu/obct/connectivity/#third)

This is part of an academic work of *94-870 Telling Stories with Data* (Spring 2024) at Carnegie Mellon University.

## DEVELOPMENT

The original visualization is already an awesome, aesthetic piece of work, but I noticed some room for improvement at least for the main interactive map.

The geographic visualization is especially useful for the audience to navigate to the data (s)he wants: much better than a chart where one has to 'search' through the country names. However, the linear, equal-interval scale of connection speed in Mbps is questionable in terms of heuristic perceptibility. Assuming that the main audience is people with minimal-to-none sense of how much data we download during daily activities, the scale should be based on the qualitative user experience, not a numeric delivery of data.

## DATA SOURCES

Internet speed data from the original author's GitHub.
[github.com](https://github.com/EDJNet/internet_speed)

Geospatial data of European borderlines from the Technical University of Denmark(DTU).
[data.dtu.dk](https://data.dtu.dk/articles/dataset/Shapefile_of_European_countries/23686383)

Novel data were appended to the original file(.shp) from DTU: the polygon for Austria was missing.
The Author's data(.csv) were modified to be joined with DTU's as a single feature data via Visual Studio Code and ArcGIS Pro.
Data that do not align with each other (i.e. some countries not being in the EU) were omitted due to the nature of this project.


