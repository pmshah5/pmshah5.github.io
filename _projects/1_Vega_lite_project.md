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

Followin is an image showing the crash data distribution from 2014 to 2023 in Chicago MPA. I prepared this graph using pandas and matplotlib in python. Here is the link for the notebook. [Link](https://github.com/pmshah5/pmshah5.github.io/blob/main/python_notebooks/Project_5.ipynb)

<div class="left">
{% include elements/button.html link="https://data.cityofchicago.org/Transportation/Traffic-Crashes-Crashes/85ca-t3if/data" text="Data Source" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/pmshah5/pmshah5.github.io/blob/main/python_notebooks/Project_5.ipynb" text="Python File" %}
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


Interactive visualization 1

<vegachart schema-url="{{ site.baseurl }}/assets/json/new_fp_1.json" style="width: 100%"></vegachart>


## Chart-2

Interactive Visuzlization 2

<vegachart schema-url="{{ site.baseurl }}/assets/json/new_fp_2.json" style="width: 100%"></vegachart>

## Chart-3


Interactive visualization 1

<vegachart schema-url="{{ site.baseurl }}/assets/json/new_fp_3.json" style="width: 100%"></vegachart>



## Write Up about Visualization.

The overall aim for the visualization is to provide various interactive charts and maps which provide detailed insights into Crash data for 2022 and 2023 data for Chicago. Three charts are prepared in combination with interactivity and without interactivity. 

Chart-1 displays the bar chart of primary cause of crash. Here top 10 causes for crash is shortlisted according to number of the crashes.The 'top_causes' variable is a Pandas created to count of the top 10 primary contributory causes of crashes in Chicago with number of Crashes.

Chart-2 displays the spatial distribution of the crashes in the Chicago area. With hovering interactivity, it will allow you to check the information about the primary cause of crash and year. The data is 
   

## Chart-3

### Contexual Visualizations

1. Champaign County Traffic Crash Dashboard
![Traffic Crash Dashboard, Champaign County](/assets/pngs/fld.png)
[Source Link](https://crashdashboard.ccrpc.org/)

2. Florida Crash Dashboard
![Traffic Crash Dashboard, Florida State](/assets/pngs/Champ_dashboard.png)
[Source Link](https://www.flhsmv.gov/traffic-crash-reports/crash-dashboard/)

