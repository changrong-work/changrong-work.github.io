---
layout: project
type: project
title: "Chicago After Dark: Where and When Reported Crime Clusters Across the City"
permalink: /projects/chicago-crime-patterns/
---

# Chicago After Dark: Where and When Reported Crime Clusters Across the City

**Author:** Changrong Wu  
**Project type:** Interactive data visualization article for the public

Chicago is a large city, and crime does not happen evenly across every place or every hour. A citywide crime total can tell us whether reported crime is rising or falling, but it does not show where incidents are concentrated, which types of crime are most common, or when those reports tend to happen. This project uses reported Chicago crime data from the past year to help a public audience explore crime patterns by location, time, and category.

The main dataset comes from the City of Chicago Data Portal's public crime records. Each row represents one reported incident. For this article, I focus on the most useful fields for public exploration: the date of the report, the primary crime type, the latitude and longitude, and the Chicago community area. I also use the City of Chicago community area boundary file so that readers can connect individual incident points to recognizable parts of the city. To keep the public-facing interactive page lightweight enough for web hosting, the map displays a random sample of incident locations, while the timeline and contextual charts are based on aggregated counts from the cleaned one-year dataset.

The interactive visualization below is designed to be read like a map-based news graphic. Use the dropdown menu to choose the whole city or one community area. Then drag across the monthly timeline to focus on a shorter period. The map and timeline work together: the map shows where sampled reports occurred, while the timeline shows whether different crime types changed over time. You can also click crime types in the legend to focus on one category.

<iframe src="/final/central_interactive_chicago_crime.html" width="900" height="870" frameborder="0"></iframe>

The first pattern to notice is that reported crime is spatially uneven. Some areas show dense clusters of sampled reports, while other parts of the city have fewer visible points. This does not automatically mean that one area is more dangerous than another, because the data only includes reported incidents and does not adjust for population, visitors, policing patterns, or land use. Still, the map is useful because it shows that crime should be understood geographically, not only as a single citywide number.

The second pattern is that different crime categories tell different stories. A general crime total can hide the fact that theft, battery, criminal damage, and other categories may follow different seasonal or neighborhood patterns. For a public reader, this matters because “crime” is not one single behavior. Looking at primary type helps separate everyday property-related reports from more serious violent categories and makes the chart easier to interpret.

<iframe src="/final/context_top_crime_types.html" width="850" height="430" frameborder="0"></iframe>

The bar chart gives context for the map by showing which crime types appear most often in the one-year dataset. This chart is not interactive because its job is simpler: it gives readers a quick baseline before they interpret the more complex map. Since the categories are names rather than continuous numbers, a bar chart is the clearest choice here.

Timing is another important part of the story. The heatmap below groups reports by day of week and hour of day. Darker cells represent more reports. This view helps readers see whether reported crime is concentrated during daytime, evening, late night, weekdays, or weekends. It also adds context to the timeline above, because a monthly pattern and an hourly pattern answer different questions.

<iframe src="/final/context_day_hour_heatmap.html" width="850" height="390" frameborder="0"></iframe>

Overall, this project shows that public crime data becomes more useful when readers can move between three levels of detail: where incidents happen, what kinds of incidents are most common, and when reports are concentrated. The interactive map is the central visualization because it lets readers explore geography and time together. The two contextual charts support the story by summarizing crime type composition and weekly timing patterns.

## Data sources and analysis notebook

- Main data: [City of Chicago Data Portal — Crimes: 2001 to Present](https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-Present/ijzp-q8t2)
- Boundary data: [City of Chicago Data Portal — Boundaries: Community Areas](https://data.cityofchicago.org/Facilities-Geographic-Boundaries/Boundaries-Community-Areas-current-/cauq-8yn6)
- Analysis notebook: [Part 3 Analysis Notebook](https://github.com/YOUR-USERNAME/YOUR-REPO/blob/main/part3_analysis_notebook.ipynb)
- Central visualization and contextual visualizations were created by the author in Python using Pandas and Altair. The notebook above contains the code used to create all three embedded HTML visualizations.

## Notes and limitations

This article uses reported incidents, so it should not be read as a complete measure of all crime. Some incidents are not reported, and reporting patterns may vary by neighborhood and crime type. The map uses a random sample of points for faster web loading and GitHub compatibility, so it should be interpreted as a visual overview of spatial patterns rather than an exact count of every incident location. The timeline, bar chart, and heatmap use aggregated counts from the cleaned one-year dataset. For a more formal public safety analysis, future work could adjust crime counts by population, visitor activity, or police district boundaries.
