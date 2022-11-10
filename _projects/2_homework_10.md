---
name: Homework 10
tools: [Python, HTML, vega-lite, Jekyll]
image: assets/pngs/cars.png
description: Homework 10 project that uses vega-lite for interactive viz!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

# Group Members
- Xiuyuan Wang: xiuyuan7
- Jing Wang: jingw13
- Yichen Huang: yichenh8



# Visualization 1
This is a visualization about building status and their size of area seperately.

<vegachart schema-url="{{ site.baseurl }}/assets/json/plot1.json" style="width: 100%"></vegachart>

This is a simple plot to show the rough sight of building-status with size of buildings, so just choose the default color. Using the median instead of average, which makes the numeric footage more scientific. The building status is just three categories: Abandon, In progress and In use.

For the encoding, field of axis y - Square Footage which is aggregated by median to clear its data accuracy, axis x is just specified as its own datatype which is the axis y field did as well.

If we analysis the relationship or other reasons to create such distribution, this simple diagram can be used as addtional resource for further researches.


# Visualization 2
This is a linked visualization about agencies' number of properties in different counties and the sum of square footages for properties each agency owns.

<vegachart schema-url="{{ site.baseurl }}/assets/json/plot2.json" style="width: 100%"></vegachart>

In this plot we have 2 diagrams that are linked together.

The upper one is a rectangular plot about the agencies and their counts of properties in each county. For the encoding of this chart, we specified the x variable and the data type, the y variable and its data type, as well as the aggregation method as count in the color parameter.

The lower one is a bar plot describing the sum of square foots of properties owned by different agencies. This is a chart that is carried on from homework 9. In the encoding part, we specified the x variable and its data type, the y variables and its aggregation type -- sum, and its data type as well. I get rid of the “tooltip“ spec for the “mark” because as this chart is linked to the upper one, this parameter would not work.

For the design of interactivity, I followed the examples given in week 10’s lecture. Readers can select data by dragging a rectangle box in the upper chart, and the chart below will only display the diagram using data chosen in the upper chart. In this way, chart readers can inspect into specific agencies and counties they are interested in. They can also check that, for a given agency, in which county they have the most areas of property. So we believe in this way, we can bring more insight into the dataset.

To make the plots work in altair, we didn't change much. We just changed the original side-by-side plot code in Vega-lite by deleting the params and transformation parameters and defined an alt.selection_interval variable in Altair.



<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/main/data/building_inventory.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/Xiuyuan7/Xiuyuan7.github.io/blob/main/python_notebooks/homework_10.ipynb" text="The Analysis" %}
</div>

