---
name: Assignment 10
tools: [Python, HTML, vega-lite]
image: assets/pngs/p_1.png
description: This is a assignment 10.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Assignment 10

Example comes from this [dataset](https://blog.4dcu.be/programming/2021/05/03/Interactive-Visualizations.html) that was also used in [our test import script](https://github.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/blob/main/week01/test_imports_week01.ipynb).

We can use a vegachart HTML tag like so:

```
<vegachart schema-url="{{ site.baseurl }}/assets/json/dashboarding.json" style="width: 100%"></vegachart>
```

<vegachart schema-url="{{ site.baseurl }}/assets/json/dashboarding.json" style="width: 100%"></vegachart>



## Description 

To prepare the above interactive dashboard we used the dataset uploaded here [link](https://github.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/raw/main/data/michigan_lld.flt) The dataset represent the land cover information for the states of USA. Here we used temprature as the parameter. The left side of the box chart is the visualization of higher side temprature range all the states. It also allow to select the box and pan move. In the right side of the dashboard, the bar chart displays the frequency for the selected bin.    




