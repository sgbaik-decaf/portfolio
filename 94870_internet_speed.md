Click [HERE](https://sgbaik-decaf.github.io/portfolio) to return to `main` page of my repo.

You can also click the blue `portfolio` button to return to `main`.

The link to the `main` is [https://sgbaik-decaf.github.io/portfolio](https://sgbaik-decaf.github.io/portfolio).

# Internet speed of European Countries

This is part of an academic work of 94-870 *Telling Stories with Data* at Carnegie Mellon University.

There is an interactive map *and* a stacked bar graph embedded in it. Wait till it loads. If prompted, log in with your CMU or ESRI account.

For iPad users: a fullscreen alternative is available [here](https://carnegiemellon.maps.arcgis.com/apps/instant/sidebar/index.html?appid=0781e9e4284c41248d0303d50ab5ee02)

<iframe src="https://carnegiemellon.maps.arcgis.com/apps/instant/sidebar/index.html?appid=0781e9e4284c41248d0303d50ab5ee02" width="1000" height="700" frameborder="0" style="border:0" allowfullscreen>iFrames are not supported on this page.</iframe>

## Original Visualization

This work is based on the following visualization:

'Average internet speed across Europe' by Ornaldo Gjergji, European Data Journalism Network

[europeandatajournalism.eu](https://datavis.europeandatajournalism.eu/obct/connectivity/#third)

## Development

The original visualization is already an awesome, aesthetic piece of work, but I noticed some room for improvement in the main interactive map.

The geographic visualization is especially useful for the audience to navigate to the data (s)he wants: much better than a chart where one has to 'search' through the country names. However, the linear, equal-interval scale of connection speed in Mbps is questionable in terms of heuristic perceptibility. Assuming that the main audience is people with minimal-to-none sense of how much data we download during daily activities, the scale should be based on the qualitative user experience, not a numeric delivery of data.

Other than the reconstruction of the interactive map, a major change was redefining the color-code scale from continuous to categorical, so that the audience can easily understand what is possible and not given a certain internet download speed.

Also, I changed the color scheme from `pale green - blue` to `mustard brown - blue` to communicate that lower internet speed is a no-fun experience. I replaced the labels of countries with full names with variable visibility (no letters when zoomed out to the big picture) and added a filter showing the feasibility of "4K YouTube".

## Data Sources

Internet speed data from the original author's GitHub.

[github.com](https://github.com/EDJNet/internet_speed)

Geospatial data of European borderlines from the Technical University of Denmark(DTU).

[data.dtu.dk](https://data.dtu.dk/articles/dataset/Shapefile_of_European_countries/23686383)

Novel data were created and appended to the original file(.shp) from DTU: the polygon for Austria was missing.

The Author's data of 2022 Q1(.csv) were modified to be joined with DTU's as a single feature data via Visual Studio Code and ArcGIS Pro.

Data missing in the file were manually filled in from the original visualization.

Data that do not align with each other (i.e. some countries not being in the EU) were omitted due to the nature of this project.

## Alternative prototype (Stacked bar graph)

<div class='tableauPlaceholder' id='viz1707117626028' style='position: relative'><noscript><a href='#'><img alt='Internet speed of European countries ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;eu&#47;eu_internet_test&#47;Sheet13&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='eu_internet_test&#47;Sheet13' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;eu&#47;eu_internet_test&#47;Sheet13&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='ko-KR' /><param name='filter' value='publish=yes' /></object></div>
<script type='text/javascript'>
  var divElement = document.getElementById('viz1707117626028');
  var vizElement = divElement.getElementsByTagName('object')[0];
  vizElement.style.width='100%';vizElement.style.height=(divElement.offsetWidth*0.75)+'px';
  var scriptElement = document.createElement('script');
  scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';
  vizElement.parentNode.insertBefore(scriptElement, vizElement);
</script>

As an alternative to the map, I also came up with a stacked bar graph. Data is from the original author's [github.com](https://github.com/EDJNet/internet_speed).

The darker blue represents the average download speed while the lighter blue indicates the average upload speed.

The reasoning behind this is that I wanted to visualize both the download and upload speed at the same time: the download speed being the primary data and the upload speed as a proportion of the download speed.

Due to technical difficulties, the download speed is prompted with `AGG(AVG([avg d]) - AVG([avg u]))`.

This is the value that pops up when one hovers the mouse on the darker blue: completely not what I intented.
