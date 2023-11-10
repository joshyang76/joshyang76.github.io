---
name: HW8
tools: [Python, HTML, vega-lite]
image: assets/pngs/cars.png
description: This is a "showcase" project that uses vega-lite for interactive viz!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Example including vega-lite

Example comes from this [great blog post right here](https://blog.4dcu.be/programming/2021/05/03/Interactive-Visualizations.html) that was also used in [our test import script](https://github.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/blob/main/week01/test_imports_week01.ipynb).

We can use a vegachart HTML tag like so:

```
<vegachart schema-url="/assets/json/cars.json" style="width: 100%"></vegachart>
The first plot is a rectangular heatmap that visualizes the distribution of buildings by their status and total floors. It employs nominal encoding for 'Bldg Status' on the x-axis and quantitative binning for 'Total Floors' on the y-axis, with a color scheme highlighting the count of records, effectively representing data density. The second plot is a bar chart showcasing the distribution of buildings by the year acquired, using quantitative binning on the x-axis for 'Year Acquired' and a count on the y-axis, with a straightforward color scheme focusing on distribution. The interactivity feature, a brush selection tool, links the two plots, allowing users to select a range in the heatmap and filter corresponding data in the bar chart. This interactivity enriches the visualization, offering a dynamic way to explore and understand the relationship between different variables.
```

<vegachart schema-url="{{ site.baseurl }}/assets/json/chart.json" style="width: 100%"></vegachart>

In theory, you can also use [Jekyll hooks](https://jekyllrb.com/docs/plugins/hooks/) to do it, but I haven't figured out a way that looks nice yet.


## Search The Data & Methods

Below is where we can put some links to both the data and the analysis code as buttons:

```
<div class="left">
{% include elements/button.html link="https://github.com/vega/vega/blob/main/docs/data/cars.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://blog.4dcu.be/programming/2021/05/03/Interactive-Visualizations.html" text="The Analysis" %}
</div>
```

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://github.com/vega/vega/blob/main/docs/data/cars.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jnaiman/online_cv_public/blob/main/python_notebooks/test_generate_plots.ipynb" text="The Analysis" %}
</div>

