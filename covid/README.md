# Covid Situation Report (PowerBI)

## Intro

Since media channels are overflown with news on the COVID-19 virus it's harder and harder to see the forest from the trees so I put together my own Bi report. The report is mostly based on the "famous" dataset from the John Hopkins University and as such the data can be up to one day old.

## Screenshots

![Report Screenshot](images/covid1.png)

## Description

> **Note:** Some of the report sections have slicer with countries. The so called "select" countries is a predefined table with the countries I'm directly interested in. The report can always be changed to provide slicers for different countries.

### Report Sections

| **Section** | **Description** | **Comments** |
|-------------|-----------------|--------------|
| Trend Overview |  Overview of latest trends for (select) countries |
| Trend Details | Some details on the same data |
| Country Rank | Select countries ranked by different measures |
| Country Table | Table ranking countries by same measures |
| Country Map | Map visualization of select countries by reported cases |
| World | Map and table visualization of world wide cases |
| Italy | Italy Country Map and details (today) |
| Ireland | Ireland Country Map and details (today)  |
| France | France Country Map and details (today)  |
| Romania | Romania Country Map and details (today) |
| US | US Country Map and details (today) |
| WIP | Work in progress visualization(s) |

### Report Measures

| **Measure** | **Description** | **Inspiration** |
|-------------|-----------------|-----------------|
| Days Deaths Double | How long it has taken for the number of deaths to double in each country| [Our World in Data](https://ourworldindata.org/coronavirus#the-growth-rate-of-covid-19-deaths) / [PowerBI Doubling Time](https://www.thebiccountant.com/2020/03/22/calculating-doubling-times-with-dax-in-power-bi/) |
| Days Deaths Double | Same as above for confirmed cases |
| Death Rate | Aparent mortality (total deaths / tocal confirmed cases) | |
| Growth Rate | The % by which cases have increased (3 days average) | [CoVID Growth Rates](http://nrg.cs.ucl.ac.uk/mjh/covid19/) |
| Days to Italy (Absolute) | Days it would take each country to reach current case level in Italy based on the Growth Rate | [CoVID Growth Rates](http://nrg.cs.ucl.ac.uk/mjh/covid19/) |
| Days to Italy (Relative) | Same as above but relative to population | |
| Days to Italy Peak (Absolute) | Days it would take each country to reach peak case level in Italy based on the Growth Rate. Peak case level is the date when Italy had the highest growth rate | |
| Days to Italy Peak (Relative) | Same as above bu relative to population size | |
| Total Cases | Cumulative number of confirmed cases to date |
| (Total) Cases per mil. inhabitants | Cumulative number of cases to date divided by polulation size (1 million inhabitants) | 

## Data Sources

| **Data Source** | **Description** | **URL** |
|-----------------|-----------------|---------|
| JHU CSSE | Data repository for the 2019 Novel Coronavirus Visual Dashboard operated by the Johns Hopkins University | [GitHub CSV Files](https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_time_series) |
| NovelCOVID / API | API for Current cases and more stuff about COVID-19 | [GitHub Repo](https://github.com/novelcovid/api)|
| Coronavirus Romania Project | Romania project to track local cases | [Dashboard](https://covid19.geo-spatial.org/) |
| DataHub.io Population CSV | Population Figures by Country | [CSV](https://datahub.io/JohnSnowLabs/population-figures-by-country/r/population-figures-by-country-csv.csv) |
| France Data | Data Against COVID-19 / FR | https://opencovid19.fr/ |
| Italy Data | Italia - Monitoraggio situazione | [Dataset](https://data.world/ondata/covid-19-italia-dati-dipartimento-protezione-civile/workspace/project-summary?agentid=ondata&datasetid=covid-19-italia-dati-dipartimento-protezione-civile) & [Github](https://github.com/pcm-dpc/COVID-19) |
| Ireland Data | GeoHive OpenData Catalog | [Dataset](https://opendata-geohive.hub.arcgis.com/datasets/58f883d6f4054574a1a885acd847bd51_0) |
| US Data | NovelCOVID / API | see above |

## Inspiration

* https://ourworldindata.org/coronavirus
* https://ourworldindata.org/covid-testing
* http://nrg.cs.ucl.ac.uk/mjh/covid19/
* https://www.devex.com/news/covid-19-a-timeline-of-the-coronavirus-outbreak-96396
* https://drive.google.com/file/d/1DqfSnlaW6N3GBc5YKyBOCGPfdqOsqk1G/view
* https://www.arcgis.com/apps/opsdashboard/index.html#/bda7594740fd40299423467b48e9ecf6
* https://covid19.geo-spatial.org/dashboard/main
* https://qap.ecdc.europa.eu/public/extensions/COVID-19/COVID-19.html
* https://www.europeandataportal.eu/data/datasets/covid-19-coronavirus-data?locale=en
