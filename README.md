# 🏅 MTH208 Olympics Data Analysis

An R-based statistical analysis and interactive **Shiny dashboard**
exploring historical Olympic Games data, medal performance, athlete
characteristics, participation trends, and country-level socioeconomic
factors.

> **Course:** MTH208\
> **Project:** Olympics Data Analysis\

------------------------------------------------------------------------

## 🚀 Live Dashboard

### [Open the Interactive Olympics Dashboard](https://styn93-chhavi21.shinyapps.io/shiny-app/)

The dashboard is deployed as a Shiny web application, so users can
explore the analysis directly from a browser without installing R.

------------------------------------------------------------------------

## 📌 Project Overview

The Olympic Games generate a large amount of historical and
athlete-level data that can be used to investigate how Olympic
participation and performance have changed over time.

This project combines Olympic medal data with athlete demographics and
country-level socioeconomic indicators to explore:

-   How Olympic participation has changed over time
-   How medal performance varies between countries
-   Whether hosting the Olympics is associated with increased medal
    performance
-   How medal counts evolve across Olympic years
-   The age, height, and weight distributions of athletes
-   Whether country-level factors are associated with cumulative Olympic
    medal counts

The project combines **data extraction, data cleaning, statistical
analysis, visualization, and interactive web application development**
using R.

------------------------------------------------------------------------

## 🎯 Research Questions

The project investigates the following questions:

1.  **Does being the host country have an association with an increase
    in medal count?**

2.  **Is a country's total Olympic medal count associated with its
    literacy rate?**

3.  **Is Olympic medal performance associated with per-capita alcohol
    consumption?**

4.  **Is Olympic medal performance associated with beer prices?**

5.  **Does the year of independence of a country have an association
    with its Olympic medal performance?**

6.  **What country-level factors appear to be associated with Olympic
    success?**

7.  **How does a country's medal count change over the years?**

8.  **What are the age, height, and weight distributions of Olympic
    athletes?**

9.  **How has the number of participating nations changed over time?**

10. **How has the number of Olympic events changed over time?**

------------------------------------------------------------------------

# 📊 Interactive Dashboard

The main application is located in:

``` text
Shiny-App/
├── app.R
├── helpers.R
├── data/
├── plots/
└── graphics/
```

The dashboard contains the following sections.

### 1. Introduction

Provides an overview of Olympic participation and displays trends in:

-   Number of participating nations
-   Number of events
-   Male and female athlete participation over time

### 2. Race for Medals

Allows users to select countries and compare Olympic medal performance.

The analysis includes:

-   Gold medals
-   Silver medals
-   Bronze medals
-   Total medals
-   Country-level comparisons

### 3. Evolution of Medals

Allows a user to select a country and investigate how its Olympic medal
performance has changed across different years.

The section also examines the relationship between medal performance and
hosting the Olympics.

### 4. Olympics Data

Provides an interactive exploration of historical Olympic results.

Users can filter by:

-   Season
-   Year
-   Sport
-   Event

The dashboard displays:

-   Top medal-winning teams
-   Medal breakdowns
-   Event-level medal summaries
-   Host/event information

### 5. Distribution

Explores athlete characteristics for a selected country.

Variables include:

-   Age
-   Height
-   Weight
-   Sex

The dashboard uses distributions to show how athlete characteristics
vary across countries.

### 6. Interesting Factors

Explores relationships between cumulative Olympic medal counts and
country-level variables, including:

-   Life expectancy
-   Beer price
-   Per-capita alcohol consumption
-   Year of independence
-   Suicide rate
-   Unemployment rate
-   Literacy rate
-   Forest area
-   Population

These analyses are exploratory. **Correlation should not be interpreted
as proof of causation.**

------------------------------------------------------------------------

# 🗂️ Project Structure

``` text
MTH208_Olympics_project-main/
│
├── README.md
├── group-project-group-22.Rproj
│
├── Data-Init/
│   ├── BMI.Rdata
│   ├── Host.Rdata
│   ├── Independence.Rdata
│   ├── LifeExp.Rdata
│   ├── Literacy_rate.csv
│   ├── alcohol.Rdata
│   ├── beer.Rdata
│   ├── forestArea.Rdata
│   ├── suicide_rates.csv
│   ├── total_medals.Rdata
│   ├── unemployment_rate.Rdata
│   └── year_wise_medals.Rdata
│
├── DataExtraction/
│   ├── BMI.R
│   ├── BeerPrice(500ml).R
│   ├── FinalTotalMedals.R
│   ├── FinalYearWiseMedals.R
│   ├── Host.R
│   ├── LifeExp.R
│   ├── alchol.R
│   ├── forestArea.R
│   ├── total_medals.R
│   └── year_wise_medals.R
│
├── Presentation/
│   ├── Group_22_Presentation.pdf
│   ├── link.Rmd
│   ├── link.html
│   └── readme.md
│
├── Reports/
│   ├── project_report.Rmd
│   ├── project_report.pdf
│   ├── data/
│   └── Analysis_files/
│
└── Shiny-App/
    ├── app.R
    ├── helpers.R
    ├── data/
    ├── graphics/
    └── plots/
```

------------------------------------------------------------------------

# 📁 Data

The project uses three main analytical datasets.

## `FinalYearWiseMedals.Rdata`

Contains year-wise Olympic medal information, including:

-   Year
-   Rank
-   Nation
-   Gold medals
-   Silver medals
-   Bronze medals
-   Total medals
-   Host nation

This dataset is used to analyse how medal performance changes over time.

------------------------------------------------------------------------

## `FinalTotalMedals.Rdata`

Contains cumulative Olympic medal counts together with country-level
demographic and socioeconomic variables.

Variables include:

-   Nation
-   Gold
-   Silver
-   Bronze
-   Total
-   Literacy
-   Population
-   Life expectancy
-   BMI
-   Alcohol consumption
-   Forest area
-   Beer price
-   Year of independence
-   Suicide rate
-   Unemployment rate

This dataset is primarily used in the correlation/factor analysis.

------------------------------------------------------------------------

## `height_age_weight.Rdata`

Contains athlete-level information including:

-   Sex
-   Age
-   Height
-   Weight
-   Nation

The dataset is used for athlete distribution analysis.

------------------------------------------------------------------------

# 🔎 Data Extraction

The `DataExtraction/` directory contains the R scripts used to collect
and prepare the supporting datasets.

The project uses **`rvest`** for web scraping and R-based data
processing.

Examples include:

``` text
BMI.R
BeerPrice(500ml).R
FinalTotalMedals.R
FinalYearWiseMedals.R
Host.R
LifeExp.R
alchol.R
forestArea.R
total_medals.R
year_wise_medals.R
```

The processed datasets required by the Shiny dashboard are already
included in the repository, so **you do not need to rerun the extraction
scripts just to launch the dashboard**.

------------------------------------------------------------------------

# 🧹 Data Preparation

The project combines information obtained from multiple sources. The
preparation process includes:

1.  Collecting Olympic medal data
2.  Extracting supporting demographic and socioeconomic data
3.  Cleaning individual datasets
4.  Standardizing country names
5.  Handling missing/incomplete observations
6.  Merging country-level datasets
7.  Creating cumulative and year-wise medal datasets
8.  Preparing datasets for visualization and interactive analysis

------------------------------------------------------------------------

# 📐 Statistical Analysis

The project mainly uses exploratory statistical analysis and
visualization.

For the country-level factor analysis, scatter plots and linear trend
lines are used to explore relationships between:

``` text
Total Olympic Medals
        ↕
Country-level factor
```

Examples include:

-   Total medals vs. life expectancy
-   Total medals vs. beer price
-   Total medals vs. alcohol consumption
-   Total medals vs. year of independence
-   Total medals vs. literacy
-   Total medals vs. population

### Important interpretation note

A correlation between two variables does **not** establish a causal
relationship.

For example:

> A country having higher life expectancy and more Olympic medals does
> not necessarily mean that higher life expectancy causes Olympic
> success.

Other factors such as population, economic development, sports
infrastructure, government investment, access to training, and
historical participation may influence both variables.

------------------------------------------------------------------------

# 🧑‍💻 Technologies Used

### Programming & Analysis

-   **R**
-   **RStudio**
-   **R Markdown**

### Data Manipulation

-   `tidyverse`
-   `dplyr`
-   `here`

### Visualization

-   `ggplot2`
-   `gridExtra`
-   `hrbrthemes`

### Interactive Dashboard

-   `shiny`
-   `shinydashboard`
-   `shinydashboardPlus`
-   `shinyWidgets`
-   `DT`

### Data Extraction

-   `rvest`

### Report / Graphics

-   `Cairo`
-   `extrafont`

------------------------------------------------------------------------

# ⚙️ Running the Project Locally

## 1. Install R

Download R from:

https://cran.r-project.org/

## 2. Install RStudio

RStudio is recommended for working with this project:

https://posit.co/download/rstudio-desktop/

## 3. Open the RStudio project

After extracting/cloning the repository, open:

``` text
group-project-group-22.Rproj
```

This opens the complete project in RStudio.

## 4. Install required packages

Run:

``` r
install.packages(c(
  "shiny",
  "shinydashboard",
  "shinydashboardPlus",
  "ggplot2",
  "tidyverse",
  "dplyr",
  "shinyWidgets",
  "here",
  "DT",
  "gridExtra",
  "hrbrthemes",
  "rvest"
))
```

For rebuilding the report, additional packages such as `Cairo` and
`extrafont` may be required.

## 5. Open the Shiny application

Open:

``` text
Shiny-App/app.R
```

The application uses relative paths such as:

``` text
data/
plots/
graphics/
```

Therefore, the `Shiny-App` directory should be the working directory
when running the app.

Check it with:

``` r
getwd()
```

If necessary:

``` r
setwd("path/to/MTH208_Olympics_project-main/Shiny-App")
```

## 6. Run the dashboard

Run:

``` r
shiny::runApp()
```

or click **Run App** in RStudio.

------------------------------------------------------------------------

# 🌐 Deployment

The dashboard can be deployed as a web application using
**shinyapps.io**.

Official documentation:

https://docs.posit.co/shinyapps.io/guide/getting_started/

After deployment, the application can be accessed through a browser
using a URL of the form:

``` text
https://<account-name>.shinyapps.io/<application-name>/
```

The deployed application contains the required R code, packages, and
data needed to run the dashboard in the cloud.

------------------------------------------------------------------------

# 📄 Project Report

The complete written statistical analysis is available in:

``` text
Reports/project_report.pdf
```

The source report is:

``` text
Reports/project_report.Rmd
```

The report covers:

-   Introduction
-   Motivation
-   Research questions
-   Data
-   Data extraction
-   Data preparation
-   Statistical analysis
-   Athlete distributions
-   Country-level factor analysis
-   Interpretation
-   Conclusions

------------------------------------------------------------------------

# 🎤 Project Presentation

The project presentation is available at:

``` text
Presentation/Group_22_Presentation.pdf
```

The original presentation link is also documented in:

``` text
Presentation/readme.md
```

------------------------------------------------------------------------

# 📚 Data Sources

The project report documents data collected from several sources,
including:

-   Olympic medal tables
-   Olympics.com
-   Wikipedia Olympic datasets
-   World Population Review
-   Kaggle's **120 Years of Olympic History: Athletes and Results**
    dataset

Primary references documented in the original analysis include:

-   Olympic all-time medal table:\
    https://en.wikipedia.org/wiki/All-time_Olympic_Games_medal_table

-   Tokyo 2020 Olympic medals:\
    https://olympics.com/en/olympic-games/tokyo-2020/medals

-   Literacy rate data:\
    https://worldpopulationreview.com/country-rankings/literacy-rate-by-country

-   BMI by country:\
    https://en.wikipedia.org/wiki/List_of_countries_by_body_mass_index

-   Athlete dataset:\
    https://www.kaggle.com/datasets/heesoo37/120-years-of-olympic-history-athletes-and-results

------------------------------------------------------------------------

# 📌 Notes

-   The project is intended primarily as an academic statistical
    analysis and visualization project.
-   The country-level factor analysis is exploratory.
-   Correlation does not imply causation.
-   The processed datasets are included so that the Shiny application
    can be run without repeating the original data extraction process.
-   Some source datasets originate from third-party websites and should
    be treated according to their respective terms and licenses.

------------------------------------------------------------------------

# 🔐 Security

Do **not** commit deployment credentials to GitHub.

In particular, never upload commands containing:

``` r
rsconnect::setAccountInfo(
  name = "...",
  token = "...",
  secret = "..."
)
```

Your shinyapps.io token and secret are credentials and should remain
private.

------------------------------------------------------------------------

# 📜 License

This repository is an academic/course project.

Unless a separate license file is added, the repository should be
considered **all rights reserved by the project authors**, subject to
the licenses/terms of the third-party datasets and resources used in the
project.

------------------------------------------------------------------------

## ⭐ If you found this project useful

Feel free to explore the source code, statistical report, and
interactive dashboard.

**Live Dashboard:** [Open the Olympics Dashboard](https://styn93-chhavi21.shinyapps.io/shiny-app/)

**Project Report:** `Reports/project_report.pdf`

**Presentation:** `Presentation/Group_22_Presentation.pdf`
