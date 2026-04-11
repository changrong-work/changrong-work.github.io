---
layout: default
title: UFO Visualization Project
---

# UFO Sightings Visualization

## Plot 1: UFO Sightings Over Time

<iframe src="chart1.html" width="700" height="500" frameborder="0"></iframe>

This visualization shows the number of UFO sightings over time. I used a line chart where the x-axis encodes time (year extracted from the datetime field) and the y-axis represents the number of sightings using a count aggregation. This encoding is appropriate because it clearly shows trends over time. No complex data transformation was required beyond converting the datetime column into a temporal format and using aggregation.

---

## Plot 2: UFO Sightings in the United States (Interactive Map)

<iframe src="chart2.html" width="700" height="500" frameborder="0"></iframe>


This visualization shows UFO sightings across the United States using geographic coordinates. Each point represents a reported sighting, plotted using latitude and longitude. I used color encoding to represent different UFO shapes, allowing viewers to distinguish between categories.

To enhance the visualization, I added a dropdown menu that allows users to select a specific UFO shape. When a shape is selected, the corresponding points are highlighted while other points are faded using opacity. This interaction helps users focus on a specific category and makes spatial patterns easier to interpret.

---

## Interactivity

The dropdown selection improves the visualization by allowing users to explore the dataset interactively. Instead of viewing all categories at once, users can highlight a specific UFO shape and better understand its geographic distribution. This makes the visualization clearer and more engaging compared to a static chart.

---

## Links

[The Data](https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/ufo-scrubbed-geocoded-time-standardized-00.csv)

[The Analysis](在这里粘贴你的GitHub notebook链接)
