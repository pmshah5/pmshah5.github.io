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


## Chiacgo Crash Data

The Traffic Crashes - Crashes dataset available on the City of Chicago's data portal contains detailed information about motor vehicle crashes reported to the police department within the city limits. The dataset includes data on various factors that contribute to crashes, such as weather conditions, types of vehicles involved, and driver actions. Additionally, it provides information about the severity of each crash and the number of injuries or fatalities that resulted. This dataset is an important resource for researchers, policymakers, and city officials who are interested in improving traffic safety and reducing the number of crashes on Chicago's streets. With over 1.1 million records spanning from 2014 to the present, this dataset offers a comprehensive view of traffic crashes in the city and can help inform evidence-based interventions to prevent future accidents.

Followin is an image showing the crash data distribution from 2014 to 2023 in Chicago MPA. I prepared this graph using pandas and matplotlib in python. Here is the link for the notebook. [Link](https://data.cityofchicago.org/Transportation/Traffic-Crashes-Crashes/85ca-t3if/data)

<div class="left">
{% include elements/button.html link="https://data.cityofchicago.org/Transportation/Traffic-Crashes-Crashes/85ca-t3if/data" text="Data Source" %}
</div>

<div class="right">
{% include elements/button.html link="https://data.cityofchicago.org/Transportation/Traffic-Crashes-Crashes/85ca-t3if/data" text="Python File" %}
</div>
<br>
<br>
<br>

![Crash Data Distribution 2013-2023, Chicago MPA](/assets/pngs/crash_1.png)

In this dataset there are 716720 accidents information provided from 2013 till today. However, It is important to notice here that crash information for 2013 and 2014 is not included in this dataset. Therefore, the crash dataset contains information from 2015 till today. There are total 49 columns which provide different details related to specific information. Information like spatial location, crash type, primary cause, fatality, speed, weather condition, road condition, day, month and time of accident is provided for 716720 accidents. 
While looking at the crash trend from 2015-2022, number of crashes were increasing exponentially. 

#### Pre-data Processing & Datafile size related issues

- Due to the large size of the dataset (>300 MB), it required large amount of space, computational resources and more time. I tried to create interactive chart using the full dataset several times. However, my system couldn't handle it and causing an frequent crash. 

- While using an online API, to directly use the file, it only allow to access 5000 datapoints without API token. Therefore, I have decided to prepare the visualization only using 2022 & 2023 data. These last 1.5 year data have approximatly 1,40,000 crash datapoints. Overall, handling and processing of filtered dataset was also difficult and complex task for me which require more computation resources and time. 

- The original python file which I used to access the data, create maps and visualization was large in size (>230 MB). Therefore, I have uploaded copy of the jupyter notebook without running it to save the space.

- While creating json file using the filter dataset, I also struggled due to large file size. Interactive json file for 2nd and 3rd chart is larger than 200 MB. Therefore, I have used GitLFS tools to upload it online for the website rendering purpose.

## Chart-1
We can use a vegachart HTML tag like so:


<vegachart schema-url="{{ site.baseurl }}/assets/json/fp_1.json" style="width: 100%"></vegachart>



## Chart-2

To prepare the above interactive dashboard we used the dataset uploaded here [link](https://github.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/raw/main/data/michigan_lld.flt) The dataset represent the land cover information for the states of USA. Here we used temprature as the parameter. The left side of the box chart is the visualization of higher side temprature range all the states. It also allow to select the box and pan move. In the right side of the dashboard, the bar chart displays the frequency for the selected bin.    

## Chart-3

### Contexual Visualizations

- Champaign County Traffic Crash Dashboard
![Traffic Crash Dashboard, Champaign County](/assets/pngs/fld.png)
[Link for the Dashboard](https://crashdashboard.ccrpc.org/)

- Florida Crash Dashboard
![Traffic Crash Dashboard, Florida State](/assets/pngs/Champ_dashboard.png)
[Link for the Dashboard](https://www.flhsmv.gov/traffic-crash-reports/crash-dashboard/)

