# IBM Data Science Professional Certificate Capstone Project: Using Data Science Concepts to Optimize Rocket Launches

## Table of Contents
* [Introduction](#introduction)
* [Code and Resources Used](#code-and-resources-used)
* [Summary of Methodologies and Results](#summary-of-methodologies-and-results)
    * [Data Collection](#data-collection)
    * [Data Wrangling](#data-wrangling)
    * [Exploratory Data Analysis](#exploratory-data-analysis)
    * [Geospatial Analysis with Folium](#geospatial-analysis-with-folium)
    * [Dashboard Visualization with Plotly Dash](#dashboard-visualization-with-plotly-dash)
    * [Predictive Modelling with Machine Learning](#predictive-modelling-with-machine-learning)
* [Discussion and Next Steps](#discussion-and-next-steps)

## Introduction

<ul>
    <li>Amalgamated several data science topics to extract and visualize data from SpaceX, and, serving in a hypothetical data scientist role, helped the hypothetical aerospace company SpaceY optimize the success of their rocket launches (and thus save money) through predictive modelling. </li>
    <li>Presented findings and insights in an attached PowerPoint presentation, mirroring presentations that would be presented to executives and non-technical audiences. </li>
    <li>Part of IBM's Data Science Professional Certificate Program.</li>
    <li>Draws upon several data science topics:</li>
  <ul>
    <li>Data collection</li>
    <li>Data wrangling</li>
    <li>Exploratory Data Analysis with Pandas and SQL queries</li>
    <li>Data Visualization with Matplotlib and Folium</li>
    <li>Dashboarding with Plotly Dash</li>
    <li>Predictive Modelling with Machine Learning</li>
    <li>Communicating and Presenting to Non-Technical Audiences</li>
  </ul>
</ul>

## Code and Resources Used
  <ul>
    <li><b>IDEs Used:</b> Google Colab, Jupyter Notebook</li>
    <li><b>Python Version:</b> 3.10.12</li>
    <li><b>SQL tool:</b> sqlite3 </li>
    <li><b>SQL queries and functions:</b></li>
         <ul>
    <li>SELECT DISTINCT</li>
    <li>FROM</li>
    <li>ORDER BY</li>   
    <li>SELECT *</li>
    <li>WHERE</li>
    <li>LIKE</li>
    <li>LIMIT</li>
    <li>SELECT SUM() AS</li>
    <li>SELECT MIN() AS</li>
    <li>BETWEEN</li>
    <li>COUNT(*)</li>
    <li>GROUP BY</li>
    <li>SELECT MAX()</li>
    <li>SELECT substr()</li>
         </ul>
    <li><b>Presentation tool:</b> Microsoft 360 PowerPoint</li>
    <li><b>Libraries and Packages:</b></li>
      <ul>
    <li><b>Data collection via API:</b>requests, pandas, numpy</li>
    <li><b>Data collection via webscraping:</b> sys, requests, BeautifulSoup, re, unicodedata, pandas</li>
    <li><b>Data wrangling:</b> pandas, numpy</li>
    <li><b>Exploratory Data Analysis with SQL queries:</b>csv, sqlite3, prettytable</li>
    <li><b>Exploratory Data Analysis with Pandas and Matplotlib:</b> pandas, numpy, seaborn, matplotlib</li>
    <li><b>Data Visualization with Folium:</b> folium (including MarkerCluster, MousePosition, DivIcon), wget, pandas </li>
    <li><b>Dashboarding with Plotly Dash:</b> pandas, dash (including dash_html_components, dash_core_components, Input, Output), plotly.express</li>
    <li><b>Predictive Modelling with Machine Learning:</b> pandas, numpy, seaborn, matplotlib, sklearn (including preprocessing, train_test_split, GridSearchCV, LogisticRegression, SVC, DecisionTreeClassifier, KNeighborsClassifier)</li>
      </ul>
  </ul>

## Summary of Methodologies and Results

#### Data Collection
<p><b>Process (data collection from API):</b> </p>
<ul>
   <li>First, use the request library to parse the SpaceX launch data from the SpaceX API (https://api.spacexdata.com/v4/rockets/)</li>
   <li>Second, use pandas to filter for Falcon 9 launches and deal with missing values.</li>
</ul>
<p><b>Process (data collection from webscraping):</b> </p>
<ul>
   <li>First, use the request library to scrape data from Falcon 9's Wikipedia article  (https://en.wikipedia.org/wiki/List_of_Falcon_9_and_Falcon_Heavy_launches)</li>
   <li>Second, extract all column/variable names from the HTML table header</li>
   <li>Third, create a data frame by parsing the launch HTML tables</li>
</ul>

#### Data Wrangling
<p>Exploratory Data Analysis (EDA) and data cleaning (e.g., checking for null values) were performed on the dataset. The results allowed us to summarize the following: raw launch count by site, number and occurrences of each orbit type and mission outcomes.​ The last step was creating a landing outcome label from the Outcome column of the dataset.​</p>

#### Exploratory Data Analysis

<p>Space X uses 4 different launch sites: CCAFS LC-40, CCAFS SLC-40, KSC LC-39A, VAFB SLC-4E​. The success rate for each site improved over time. ​Very high success rate for payloads over 8000 kg for launch sites, and 9000 kg for orbits.​ Orbit types ES-L1, GEO, HEO, and SSO are the most successful orbit types.​ Total payload mass for NASA launches: 111,268 kg.</p>

#### Geospatial Analysis with Folium

<p>The sites were concentrated in the coastal part of Southern California and Florida, possibly due to safety considerations in the event of a failed launch, which allows debris to have a better chance of falling into the ocean rather than highly populated centres.​ Despite the relative isolation, there is sufficient infrastructure in the vicinity of the launch sites to help sustain them.</p>

![image](https://github.com/user-attachments/assets/1bc051b7-b6de-400d-9898-1bc4f6d74933)

![image](https://github.com/user-attachments/assets/9259c91b-430f-4b94-b94c-8eb39b326149)

#### Dashboard Visualization with Plotly Dash
<p>Making up 41.7% of the total number of successful launches, KSC LC-39A is the most successful site when using that metric, followed by CCAFS LC-40 with 29.2%.</p>

![image](https://github.com/user-attachments/assets/40185f60-93b2-4261-ae1d-e5dd428d1f1c)

#### Predictive Modelling with Machine Learning

<p>Decision Tree Classifier, despite having the lowest test accuracy, had by far the highest accuracy overall, suggesting that it is the machine learning algorithm that SpaceY should deploy for higher accuracy in predicting successful landings and launches.</p>

![image](https://github.com/user-attachments/assets/df1c92a6-6770-4093-8cc2-83fecbec77f1)


## Discussion and Next Steps

This research proves that data science is a versatile and multi-sectoral field with use cases beyond the business world and Big Tech. In this case, it has significantly helped SpaceY using data parsing and visualization techniques, as well as predictive modelling, to help plan successful rocket launches. The next steps that SpaceY could take includes establishing partnerships with manufacturers and securing government funding using the insights from this research.


