[![MIT License][license-shield]][license-url]

<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://geods.geography.wisc.edu/">
    <img src="images/geods_safegraph_nsf_logo.jpg" alt="Logo" width="400">

  <h2 align="center">Multiscale Dynamic Human Mobility Flow Dataset in the U.S. during the COVID-19 Epidemic</h2>

  <p align="center">
    GeoDS Lab, Department of Geography, University of Wisconsin-Madison.
    <br />
    <a href="https://geods.geography.wisc.edu/covid-19-physical-distancing">Website</a>
    ·
    <a href="http://geods.geography.wisc.edu/covid19/King_WA.html">View Demo</a>
  </p>
</p>

# Note
Please refer to [https://github.com/GeoDS/COVID19USFlows](https://github.com/GeoDS/COVID19USFlows) to access all tools for downloading the datasets. This repository only provides part of the dataset.

<!-- Citation -->
## Citation
If you use this dataset in your research or applications, please cite this source:


Kang, Y., Gao, S., Liang, Y.  Li, M., Rao, J. and Kruse, J. Multiscale dynamic human mobility flow dataset in the U.S. during the COVID-19 epidemic. *Scientific Data* 7, 390 (2020). [https://www.nature.com/articles/s41597-020-00734-5](https://rdcu.be/cd2Fd)
    

```
@article{kang2020multiscale,
  title     = {Multiscale Dynamic Human Mobility Flow Dataset in the U.S. during the COVID-19 Epidemic},
  author    = {Kang, Yuhao and Gao, Song and Liang, Yunlei and Li, Mingxiao and Kruse, Jake},
  journal   = {Scientific Data},
  volumn    = {7},
  issue     = {390},
  pages     = {1--13},
  year = {2020}
}
```

<!-- ABOUT THE PROJECT -->
## About The Project


Understanding dynamic human mobility changes and spatial interaction patterns at different geographic scales is crucial for monitoring and measuring the impacts of non-pharmaceutical interventions (such as stay-at-home orders) during the pandemic. In this data descriptor, we introduce an up-to-date multiscale dynamic human mobility flow dataset across the United States, with data starting from January 1st, 2019. By analyzing millions of anonymous mobile phone users’ visit trajectories to various places provided by [SafeGraph](https://www.safegraph.com/), the daily and weekly dynamic origin-to-destination (O-D) population flows are computed, aggregated, and inferred at three geographic scales: census tract, county, and state. There is high correlation between our mobility flow dataset and openly available data sources, which shows the reliability of the produced data. Such a high spatiotemporal resolution human mobility flow dataset at different geographic scales over time may help monitor epidemic spreading dynamics, inform public health policy, and deepen our understanding of human behavior changes under the unprecedented public health crisis. This up-to-date O-D flow open data can support many other social sensing and transportation applications.

A full description of the methodology used for this study can be found here: [https://arxiv.org/abs/2008.12238](https://arxiv.org/abs/2008.12238).

<!-- Dataset Structure -->
## Dataset Structure
Due to the data size restriction of GitHub, we have splitted our repository into a set of small data repositories. Each data repository follows the same folder structure but only contains part of the dataset. Here are the details about each repository:   

| Data Repository | Data Type | Scale | Time Range |   
| --- | ----------- | --- | ----------- |   
|[COVID19USFlows](https://github.com/GeoDS/COVID19USFlows)|index page| --- |2019-2021|  
|[COVID19USFlows-WeeklyFlows](https://github.com/GeoDS/COVID19USFlows-WeeklyFlows)|weekly data|state, county|2019-2021|  
|[COVID19USFlows-WeeklyFlows-Ct2019](https://github.com/GeoDS/COVID19USFlows-WeeklyFlows-Ct2019)|weekly data|census tract|2019|  
|[COVID19USFlows-WeeklyFlows-Ct2020](https://github.com/GeoDS/COVID19USFlows-WeeklyFlows-Ct2020)|weekly data|census tract|2020|  
|[COVID19USFlows-WeeklyFlows-Ct2021](https://github.com/GeoDS/COVID19USFlows-WeeklyFlows-Ct2021)|weekly data|census tract|2021|  
|[COVID19USFlows-DailyFlows](https://github.com/GeoDS/COVID19USFlows-DailyFlows)|daily data|state, county|2019-2021|  
|[COVID19USFlows-DailyFlows-Ct2019-1](https://github.com/GeoDS/COVID19USFlows-DailyFlows-Ct2019-1)|daily data|census tract|01/2019-04/2019|  
|[COVID19USFlows-DailyFlows-Ct2019-2](https://github.com/GeoDS/COVID19USFlows-DailyFlows-Ct2019-2)|daily data|census tract|05/2019-08/2019|  
|[COVID19USFlows-DailyFlows-Ct2019-3](https://github.com/GeoDS/COVID19USFlows-DailyFlows-Ct2019-3)|daily data|census tract|09/2019-12/2019|  
|[COVID19USFlows-DailyFlows-Ct2020-1](https://github.com/GeoDS/COVID19USFlows-DailyFlows-Ct2020-1)|daily data|census tract|01/2020-04/2020|  
|[COVID19USFlows-DailyFlows-Ct2020-2](https://github.com/GeoDS/COVID19USFlows-DailyFlows-Ct2020-2)|daily data|census tract|05/2020-08/2020|  
|[COVID19USFlows-DailyFlows-Ct2020-3](https://github.com/GeoDS/COVID19USFlows-DailyFlows-Ct2020-3)|daily data|census tract|09/2020-12/2020|  
|[COVID19USFlows-DailyFlows-Ct2021](https://github.com/GeoDS/COVID19USFlows-DailyFlows-Ct2021)|daily data|census tract|01/2021-04/2021|  

## Field Descriptions
A description of all attributes in the database is shown below:  

#### Weekly Flow Data (folder: weekly_flows)
geoid\_o - Unique identifier of the origin geographic unit (census tract, county, and state). Type: string.   
geoid\_d - Unique identifier of the destination geographic unit (census tract, county, and state). Type: string.   
lat\_o - Latitude of the geometric centroid of the origin unit. Type: float.   
lng\_o - Longitude of the geometric centroid of the origin unit. Type: float.   
lat\_d - Latitude of the geometric centroid of the destination unit. Type: float.   
lng\_d - Longitude of the geometric centroid of the destination unit. Type: float.   
date\_range - Date range of the records. Type: string.   
visitor\_flows - Estimated number of visitors detected by SafeGraph between the two geographic units (from geoid\_o to geoid\_d). Type: float.   
pop\_flows - Estimated population flows between the two geographic units (from geoid\_o to geoid\_d), inferred from visitor\_flows. Type: float.  

#### Daily Flow Data (folder: daily_flows)
geoid\_o -  Unique identifier of the origin geographic unit (census tract, county, and state). Type: string.  
geoid\_d - Unique identifier of the destination geographic unit (census tract, county, and state). Type: string.  
lat\_o - Latitude of the geometric centroid of the origin unit. Type: float.  
lng\_o - Longitude of the geometric centroid of the origin unit. Type: float.  
lat\_d - Latitude of the geometric centroid of the destination unit. Type: float.  
lng\_d - Longitude of the geometric centroid of the destination unit. Type: float.  
date - Date of the records. Type: string.  
visitor\_flows - Estimated number of visitors between the two geographic units (from geoid\_o to geoid\_d). Type: float.  
pop\_flows - Estimated population flows between the two geographic units (from geoid\_o to geoid\_d), inferred from visitor\_flows. Type: float.  

#### Weekly Country Flow Data (folder: weekly_country_flows)
We provide a new dataset that contains flows from other countries to U.S.    
geoid\_o - Two-letter country codes of the origin country. Type: string.   
geoid\_d - Unique identifier of the destination geographic unit in the United States (census tract, county, and state). Type: string.   
lat\_d - Latitude of the geometric centroid of the destination unit. Type: float.   
lng\_d - Longitude of the geometric centroid of the destination unit. Type: float.    
visitor\_flows - Estimated number of visitors detected by SafeGraph between the two geographic units (from geoid\_o to geoid\_d). Type: float.   
date\_range - Date range of the records. Type: string.  

<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.



<!-- CONTACT -->
## Contact

Song Gao - [@gissong](https://twitter.com/gissong) - song.gao at wisc.edu  
Yuhao Kang - [@YuhaoKang](https://twitter.com/YuhaoKang) - yuhao.kang at wisc.edu  

Project Link: [https://github.com/GeoDS/COVID19USFlows](https://github.com/GeoDS/COVID19USFlows)  



<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements
* [SafeGraph](https://www.safegraph.com/)
* [GeoDS Lab](https://geods.geography.wisc.edu/)

## Funding
We would like to thank the funding support provided by the National Science Foundation (Award No. BCS-2027375). Any opinions, findings, and conclusions or recommendations expressed in this material are those of the author(s) and do not necessarily reflect the views of the National Science Foundation. Support for this research was partly provided by the University of Wisconsin - Madison Office of the Vice Chancellor for Research and Graduate Education with funding from the Wisconsin Alumni Research Foundation.

<!-- MARKDOWN LINKS & IMAGES -->
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=flat-square
[license-url]: https://github.com/GeoDS/COVID19USFlows/blob/master/LICENSE.txt
