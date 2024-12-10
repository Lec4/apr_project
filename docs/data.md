---
layout: default   # This tells Jekyll to use the default layout (from the theme)
title: "Data Description" # Title of the page
---

# Data Description

## Dataset Overview

The dataset used in this analysis is the **2020 NCAA Division I Academic Progress Rate Dataset**, which contains information about Academic Progress Rates for all Division I athletic teams through the year 2019. The data includes various features that may have influenced a team's Academic Progress Rate, such as conference, public/private school, and squad size.

- **Source**: The dataset is publicly available on [NCAA Website](https://www.ncaa.org/sports/2016/12/14/shared-ncaa-research-data.aspx).

## Data Attributes

The dataset consists of the following columns:

| Column Name   | Description                                                                 |
|---------------|-----------------------------------------------------------------------------|
| `SCL_NAME`| Official name of institution|
| `SPORT_CODE`| Sport identification (in code) |
| `SPORT_NAME`| Sport name|
| `CONFNAME_19`| Name of institution’s primary conference.|
| `SCL_HBCU`| Indicates if the institution is a historically black college or university (Coding: 1 = Yes; 0= No)|
| `SCL_PRIVATE`| Indicates whether the institution is private or public (Coding: 1 = Private; 0 = Public)|
| `MULTIYR_APR_RATE_1000_OFFICIAL`| The final Four-year raw or team-size adjustment APR value (on 1,000-point scale)|
| `MULTIYR_ELIG_RATE`| Four-year eligibility rate on 1,000-point scale |
| `MULTIYR_RET_RATE`| Four-year retention rate on 1,000-point scale |
| `MULTIYR_SQUAD_SIZE`| Four-year squad size |
| `PUB_AWARD_20`| Public recognition award for 2018-19 academic year, awarded in 2020 (Coding: 1 = team received award; 0 = team did not receive award) |
| `Gender_Sport | Indicates what gender sports team it is (1= Men's sports teams, 0= Women's sports teams, 2= Mixed) |


