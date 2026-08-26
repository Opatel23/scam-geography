# Data dictionary

The file `data/state_panel_2022_2025.csv` contains one observation for each U.S. state or the District of Columbia in each year from 2022 through 2025.

| Variable | Definition |
|---|---|
| `year` | FBI IC3 reporting year |
| `state` | State or District of Columbia |
| `complaints` | Number of reported IC3 complaints |
| `losses` | Total reported IC3 loss in current dollars |
| `acs_year` | ACS year used for lagged characteristics |
| `fips` | Two-digit state FIPS code |
| `population` | ACS population estimate |
| `median_income` | ACS median household income |
| `age65_count` | Estimated population age 65 or older |
| `households` | Total households |
| `internet_households` | Households with an internet subscription |
| `age65_pct` | Population age 65 or older as a percentage |
| `internet_pct` | Households with internet subscriptions as a percentage |
| `complaints_per_100k` | Reported complaints divided by population, multiplied by 100,000 |
| `loss_per_capita` | Reported loss divided by population |
| `loss_per_complaint` | Reported loss divided by complaints |
| `region` | Census-style geographic region |

## Important interpretation note

The dataset describes reported complaints and reported losses. It does not measure the complete incidence of fraud because not every victim reports to IC3 and reporting behavior may vary geographically.

