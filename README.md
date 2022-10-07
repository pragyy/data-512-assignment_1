![Language](https://img.shields.io/badge/language-python-blue.svg)
[![GitHub license](https://img.shields.io/github/license/Naereen/StrapDown.js.svg)](https://github.com/pragyy/data-512-assignment_1/blob/main/LICENSE)
![contributors](https://img.shields.io/github/contributors/pragyy/data-512-assignment_1.svg) 
![codesize](https://img.shields.io/github/languages/code-size/pragyy/data-512-assignment_1.svg) 

# Article Page Views

## Project Overview
The aim of this project is to construct, analyze, and publish a dataset of monthly article traffic for a select set of pages from English Wikipedia from January 1, 2015 through September 30, 2022. 

## Codes and Resources Used

- Editor used: VS code
- Python version: 3.9.4
- Pageviews API documentation: [Documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews) 

## Python Packages Used

- General Purpose: json, time, urllib.parse, requests
- Data Manipulation: pandas, datetime
- Visualisation: seaborn, matplotlib
- Miscelleneous: warnings

## Data Acquisition

The dinosaur data set is fetched using Wikimedia APIs calls. The data is acquired for 3 different access - desktop, mobile-app and mobile-web. Then later merged them together. 

Then later the following data files are generated that are stored in `output_data` folder.
- **Monthly mobile access -** The API separates mobile access types into two separate requests, the sum of these to make one count for all mobile pageviews. 
- **Monthly desktop access -** Monthly desktop page traffic is based on one single request. 
- **Monthly cumulative -** Monthly cumulative data is the sum of all mobile, and all desktop traffic per article.

## Analysis
The basic visual analysis are performed for the specific subsets of the data as a timeseries.

- **Maximum Average and Minimum Average -** Time series for the articles that have the highest average page requests and the lowest average page requests for desktop access and mobile access.
![maxmin](./pic/Fewest%20Months%20of%20Data.png)
- **Top 10 Peak Page Views -** Time series for the top 10 article pages by largest (peak) page views over the entire time by access type. You first find the month for each article that contains the highest (peak) page views, and then order the articles by these peak values.
![top10](./pic/Top%2010%20Peak%20Page%20Views.png)
- **Fewest Months of Data -** The third graph shows pages that have the fewest months of available data.
![fewmonths](./pic/Fewest%20Months%20of%20Data.png)

## Licenses

Source Data License: [Wikimedia Rest API](https://wikimedia.org/api/rest_v1/#/Pageviews_data/get_metrics_pageviews_aggregate_project_access_agent_granularity_start_end), licensed under [CC-BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/) and [GFDL](https://www.gnu.org/licenses/fdl-1.3.html)

Wikimedia Foundation REST API terms of use: [Wikimedia Terms & Conditions](https://www.mediawiki.org/wiki/Wikimedia_REST_API#Terms_and_conditions)
