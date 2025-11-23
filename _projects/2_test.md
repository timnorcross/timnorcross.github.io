---
name: Homework 5
tools: [Python, HTML, vega-lite]
image: assets/pngs/hw5.png
description: This is my project for HW 5
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


<vegachart schema-url="{{ site.baseurl }}/assets/json/hw5chart1.json" style="width: 100%"></vegachart>

This first plot visualizes the count of the seasons, on the right, for a given area of the data on the left. Each point on the left maps to a latitude and longitude. Specific points can be chosen by dragging a window over the data on the left, and the corresponding season counts will update on the right box plot. The interactivity helps here because you can drag the window to view different parts of the country, exploring seasonal sighting trends that way, or you can slowly drag the window horizontally or vertically to explore how the seasons change relative to latitude and longitude. Exploring this relative difference between regions would be difficult without the aid of interactivity. The underlying dataset for this visualization is a file of bigfoot sighting reports across the United States. Both the x and y axes, longitude and latitude, are encoded as quantitative because they are continuous and numeric, and also because there is no need to display each individual value. The season count axis is similarly encoded because it is a numeric count of season. Season is encoded as a nominal type because it is both discrete and unordered. The color of both the mapped data and the boxplot are mapped to the _season_ column of the data, because possible relationships between location and season is what this chart is trying to visualize. Altair automatically asigns each of the unique values a distinct color. Both the qualitative and nominal columns within the data are well organized, so no data transformations were called for. Many rows with NA values did have to be removed so as to not be included in one of the plots and not the other. 

<vegachart schema-url="{{ site.baseurl }}/assets/json/hw5chart2.json" style="width: 100%"></vegachart>

The above plot is a simple line plot of the count of reports, or rows of the data, relating to the the moon phase recorded in the reports. The idea is to see explore a relationship between sightings and the moon phase, and if one is found, this could suggest that bigfoot's activities follow a lunar cycle. Both the moon phase, as a decimal between 0 and 1, and the count of reports are quantitave type data. A color map was not necessary in this case because it is only the line of the data that is of interest. The count of reports is already sort of encoded visually as the height of the line, so color would have been redundant. Again, no data manipulation went into this plot because the axes were self explanatory and the data I was looking for were present neatly within the columns. 

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/bfro_reports_fall2022.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/timnorcross/timnorcross.github.io/blob/main/python_notebooks/Workbook_hw5.ipynb" text="The Analysis" %}
</div>

