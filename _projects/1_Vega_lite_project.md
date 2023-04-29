---
name: Final Project
tools: [Python, Alt air, vega-lite]
image: assets/pngs/Chicago_overview_map.png
description: Crash Data and Visualization for 2022 & 2023- Chicago Metropolitan Area. Image source- commons.wikimedia.org
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Crash Data and Visualization for 2022 & 2023- Chicago Metropolitan Area, IL

The primary dataset used for creating visualization is from City of Chicago Data Portal. Link for the [dataset](https://data.cityofchicago.org/Transportation/Traffic-Crashes-Crashes/85ca-t3if).


## Details of CrashData

The Traffic Crashes - Crashes dataset available on the City of Chicago's data portal contains detailed information about motor vehicle crashes reported to the police department within the city limits. The dataset includes data on various factors that contribute to crashes, such as weather conditions, types of vehicles involved, and driver actions. Additionally, it provides information about the severity of each crash and the number of injuries or fatalities that resulted. This dataset is an important resource for researchers, policymakers, and city officials who are interested in improving traffic safety and reducing the number of crashes on Chicago's streets. With over 1.1 million records spanning from 2014 to the present, this dataset offers a comprehensive view of traffic crashes in the city and can help inform evidence-based interventions to prevent future accidents.

## Chart-1
We can use a vegachart HTML tag like so:

```
<vegachart schema-url="{{ site.baseurl }}/assets/json/dashboarding.json" style="width: 100%"></vegachart>
```

<vegachart schema-url="{{ site.baseurl }}/assets/json/fp_1.json" style="width: 100%"></vegachart>



## Chart-2

To prepare the above interactive dashboard we used the dataset uploaded here [link](https://github.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/raw/main/data/michigan_lld.flt) The dataset represent the land cover information for the states of USA. Here we used temprature as the parameter. The left side of the box chart is the visualization of higher side temprature range all the states. It also allow to select the box and pan move. In the right side of the dashboard, the bar chart displays the frequency for the selected bin.    

## Chart-3

### Contexual Visualizations

- Champaign County Traffic Crash Dashboard

[Link for the Dashboard](https://crashdashboard.ccrpc.org/)

- Florida Crash Dashboard

[Link for the Dashboard](https://www.flhsmv.gov/traffic-crash-reports/crash-dashboard/)

