---
name: Final Project
tools: [Python, HTML, vega-lite, Jekyll]
image: assets/pngs/final_project_main_chart.png
description: Final project that uses vega-lite for interactive viz!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---
  
# Are people getting more inclined to purchase firearms?

## Group Members
- Xiuyuan Wang: xiuyuan7
- Jing Wang: jingw13
- Yichen Huang: yichenh8


## Central vis

<vegachart schema-url="{{ site.baseurl }}/assets/json/final_project_main_chart.json" style="width: 100%"></vegachart>



<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/BuzzFeedNews/nics-firearm-background-checks/master/data/nics-firearm-background-checks.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/Xiuyuan7/Xiuyuan7.github.io/blob/main/python_notebooks/final_project.ipynb" text="The Analysis" %}
</div>
