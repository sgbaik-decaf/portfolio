# Internet speed of European Countries

Click blue `portfolio` to return to `main`.

There is an interactive map embedded in it. Wait till it loads. If prompted, log in with your CMU or ESRI account.

For iPad users: a fullscreen alternative is available [here](https://carnegiemellon.maps.arcgis.com/apps/instant/sidebar/index.html?appid=0781e9e4284c41248d0303d50ab5ee02)

<iframe src="https://carnegiemellon.maps.arcgis.com/apps/instant/sidebar/index.html?appid=0781e9e4284c41248d0303d50ab5ee02" width="1000" height="700" frameborder="0" style="border:0" allowfullscreen>iFrames are not supported on this page.</iframe>

This is part of an academic work of *94-870 Telling Stories with Data* (Spring 2024) at Carnegie Mellon University.



# ORIGINAL VISUALIZATION

Average internet speed across Europe

Ornaldo Gjergji, European Data Journalism Network

[europeandatajournalism.eu](https://datavis.europeandatajournalism.eu/obct/connectivity/#third)



# DEVELOPMENT

The original visualization is already an awesome, aesthetic piece of work, but I noticed some room for improvement in the main interactive map.

The geographic visualization is especially useful for the audience to navigate to the data (s)he wants: much better than a chart where one has to 'search' through the country names. However, the linear, equal-interval scale of connection speed in Mbps is questionable in terms of heuristic perceptibility. Assuming that the main audience is people with minimal-to-none sense of how much data we download during daily activities, the scale should be based on the qualitative user experience, not a numeric delivery of data.

Other than the reconstruction of the interactive map, the main change is redefining the color-code scale from continuous to categorical, so that the audience can easily understand what is possible and not given a certain internet download speed.

Also, I changed the color scheme from `pale green - blue` to `mustard brown - blue` to communicate that lower internet speed is a no-fun experience. 

I replaced the labels of countries with full names with variable visibility (no letters when zoomed out to the big picture) and added a filter showing the feasibility of "4K YouTube", following the recommendation of two testers.



### Tester A (late 10's, college student) commented as below.

1. How long did it take for you to recognize what this is for?

10 seconds.

2. Is there anything you find confusing?

There is too much word on the legend.

3. Is there anything you find aesthetically unpleasant? Please rate this visualization on a 5-level scale.

4.9 / 5

5. Is there anything you would change or do differently?

It could have been better if you focused on one thing such as "4K YouTube".



### Tester B (early 30's, post-doctorate researcher) commented as below.

1. How long did it take for you to recognize what this is for?

10 seconds.

2. Is there anything you find confusing?

The abbreviated 3-letter country names obscure the map. Good otherwise.

3. Is there anything you find aesthetically unpleasant? Please rate this visualization on a 5-level scale.

4.5 / 5. I like the typeface but I don't think it's needed in the first place.

5. Is there anything you would change or do differently?

The background does not match with the actual data layer. Do we need a background map? Try using Python to ... ... (technical advice).



# DATA SOURCES

Internet speed data from the original author's GitHub.

[github.com](https://github.com/EDJNet/internet_speed)

Geospatial data of European borderlines from the Technical University of Denmark(DTU).

[data.dtu.dk](https://data.dtu.dk/articles/dataset/Shapefile_of_European_countries/23686383)

Novel data were created and appended to the original file(.shp) from DTU: the polygon for Austria was missing.

The Author's data of 2022 Q1(.csv) were modified to be joined with DTU's as a single feature data via Visual Studio Code and ArcGIS Pro.

Data missing in the file were manually filled in from the original visualization.

Data that do not align with each other (i.e. some countries not being in the EU) were omitted due to the nature of this project.
