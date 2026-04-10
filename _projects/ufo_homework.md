---
name: UFO Sightings Visualizations
tools:
  - Python
  - Altair
  - Vega-Lite
description: Two visualizations of UFO sightings data, including an interactive chart.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

# UFO Sightings Visualizations

The first visualization shows the number of UFO sightings over time using a line chart. The x-axis encodes year, and the y-axis represents the count of sightings. A line chart was chosen because it effectively shows trends over time and highlights how sightings have increased, especially after the 1990s. In the data preparation stage, the datetime column was converted into a timestamp and a new year column was extracted. The data was then aggregated by year to compute total sightings, which also helped reduce the dataset size for visualization.

<vegachart schema-url="{{ site.baseurl }}/assets/json/ufo_plot1.json" style="width: 100%"></vegachart>

The second visualization is a bar chart showing the distribution of UFO shapes for a selected year. The x-axis encodes shape as a categorical variable, and the y-axis represents the number of sightings. Color is used to distinguish between shapes, making it easier to compare categories. The dataset was filtered to include only the most frequent shapes to avoid clutter. This visualization includes interactivity through a dropdown menu that allows the user to select a year. This interaction makes the visualization more useful by enabling focused exploration of how reported shapes vary across different years.

<vegachart schema-url="{{ site.baseurl }}/assets/json/ufo_plot2.json" style="width: 100%"></vegachart>

## Data and Analysis

{% include elements/button.html link="https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/ufo-scrubbed-geocoded-time-standardized-00.csv" text="The Data" %}

{% include elements/button.html link="https://github.com/akankshaabharambe-hub/akankshaabharambe-hub.github.io/blob/main/python_notebooks/ufo_homework.ipynb" text="The Analysis" %}
