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

## Reading the data correctly

- **Observation key:** `state` + `year`. The balanced panel covers 50 states and Washington, DC across four reporting years (204 rows).
- **Timing:** ACS characteristics are lagged one year: `acs_year = year - 1`. Rates therefore use the matched prior-year population estimate, not a same-year population denominator.
- **Money:** `losses`, `median_income`, `loss_per_capita`, and `loss_per_complaint` are dollar amounts, not thousands of dollars. Do not interpret nominal dollar changes as inflation-adjusted changes.
- **Percentages:** `age65_pct` and `internet_pct` use the 0–100 scale; 17.6 means 17.6%, not 1,760%.
- **Identifiers:** Import `fips` as text to preserve leading zeroes, such as Alabama's `01`.
- **Aggregation:** Recompute rates from summed numerators and denominators. A simple mean of state rates does not produce a population-weighted national rate.

## Economic decomposition

```text
loss_per_capita = (complaints_per_100k / 100000) × loss_per_complaint
```

This separates reported complaint frequency from average reported loss severity. A complaint is not necessarily a unique victim, so `loss_per_complaint` should not be labeled “loss per victim.”

## Source and method trail

Use the workbook's `Sources & Notes` sheet for the source trail and `Panel Models` for model specifications and uncertainty. The [project overview](README.md) summarizes findings and links to the source organizations.

## Important interpretation note

The dataset describes reported complaints and reported losses. It does not measure the complete incidence of fraud because not every victim reports to IC3 and reporting behavior may vary geographically.

