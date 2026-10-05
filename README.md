# Scam Geography

**The economics of reported internet crime across U.S. states**

A research project by **Om Patel** · 2022–2025 · 51 jurisdictions · 204 state-year observations

Why do some states report more internet-crime losses per resident than others?

Compare states in Excel to examine reported complaint rates, losses per complaint, and their relationship with income, internet access, and age structure.

**Release status:** Private review draft. The workbook and preview images still need terminology updates to match the scope described below.

The data use IC3's state-level internet-crime totals, not a fraud-only subset. These totals include fraud and other reported offenses. See the [2025 IC3 report](https://www.ic3.gov/AnnualReport/Reports/2025_IC3Report.pdf) for the distinction between all complaints and cyber-enabled fraud.

**[Get the interactive workbook](Scam_Geography_Interactive_Economics_Project.xlsx)** · [Explore the data](data/state_panel_2022_2025.csv) · [Variable definitions](DATA_DICTIONARY.md)

On the workbook page, choose **Download raw file**, then open the downloaded file in desktop Microsoft Excel. The images below are previews; the interactive controls are inside the workbook.

[Tour](#take-a-five-minute-tour) · [Findings](#what-the-evidence-suggests) · [Methods](#data-and-methods) · [Limitations](#limits-of-the-analysis) · [Citation](#cite-this-project)

![Scam Geography overview with research question, coverage, and economic framework](images/start-here.png)

## Take a five-minute tour

| Step | Worksheet | Try it |
| --- | --- | --- |
| 1 | Start Here | Read the research question and the guide to the evidence. |
| 2 | Interactive Econ Lab | Compare North Carolina with California. Change the year and outcome using the cream input cells. |
| 3 | State Scorecard | Choose a state and examine its exposure, severity, percentile, and rank. |
| 4 | Scenario Lab | Enter a hypothetical income change and compare the three model implications. |
| 5 | Panel Dashboard | Compare the national trend with regional results, then review the model limitations. |

**Try a two-minute investigation:** Compare North Carolina with California in the same year. Note which has higher loss per resident, then switch to complaints per 100,000 and loss per complaint. Does complaint frequency, loss severity, or both explain the difference? Change the year to see whether the pattern holds.

<details>
<summary><strong>Preview the interactive comparison lab</strong></summary>

Compare two states across years and outcomes. Percentage gaps and a four-year chart respond to your selections; the model summary provides context for interpreting the evidence.

![Interactive comparison lab with year, state, and outcome selectors](images/interactive-econ-lab.png)

</details>

<details>
<summary><strong>Preview the state scorecard and scenario lab</strong></summary>

The scorecard places a selected jurisdiction in the distribution of reported exposure, loss severity, and overall harm. Its exposure–severity quadrant shows whether a ranking reflects complaint frequency, average reported loss severity, or both.

![State scorecard with percentile measures and exposure–severity quadrant](images/state-scorecard.png)

The scenario lab translates estimated income elasticities into model-implied changes in loss per person. Use it to explore sensitivity to model choice. These associations do not establish the effect of an income policy.

![Scenario lab comparing baseline and model-implied loss per person](images/scenario-lab.png)

</details>

## The economic framework

> **Reported loss per person = complaints per person × reported loss per complaint**

This accounting identity separates reported exposure from severity:

- **Reported exposure:** complaints relative to population.
- **Severity:** dollars lost per reported complaint.

Complaint rates displayed per 100,000 residents must be divided by 100,000 before applying the identity.

The models examine how median household income, the share of residents age 65 or older, and household internet access are associated with these outcomes. Year effects account for common annual shifts. State-and-year fixed effects examine changes within states while accounting for persistent state differences.

## What the evidence suggests

**Main takeaway:** Higher-income states tend to report greater losses per resident in cross-state comparisons; the within-state evidence is less precise. Model choice changes the size and certainty of the estimated relationship.

Reported loss per resident also increased substantially from 2022 to 2025.

| Evidence | Estimated income elasticity | Interpretation |
| --- | ---: | --- |
| Pooled model with year effects | 1.55 | Positive association in the pooled state panel. |
| Excluding Washington, D.C. | 0.89 | The positive association persists without D.C. |
| State-and-year fixed effects | 2.19 | Positive estimate, but statistically imprecise. |

**Reading the elasticity:** In the pooled model, 1% higher median household income is associated with approximately 1.55% higher reported loss per resident, holding the included controls and year effects constant. This is a percentage change, not a dollar change or a percentage-point change.

The estimates support a geographic association. They do not establish that raising income causes higher reported internet-crime losses. See `Panel Models` for standard errors, approximate p-values, and additional robustness checks.

<details>
<summary><strong>Preview the national, regional, and state dashboards</strong></summary>

![Four-year panel dashboard with national trend and all regional observations](images/panel-dashboard.png)

![State dashboard with reported loss rankings and income comparison](images/state-dashboard.png)

</details>

## Data and methods

The project combines FBI Internet Crime Complaint Center annual reports with U.S. Census Bureau American Community Survey estimates.

| Component | Approach |
| --- | --- |
| Coverage | 50 states and Washington, D.C.; 2022–2025 |
| Unit of analysis | State-year; 204 observations |
| Outcomes | Reported complaints, reported losses, and population-scaled measures |
| Explanatory variables | Median household income, age structure, and household internet access |
| Timing | ACS characteristics lagged one year |
| Panel models | Pooled OLS with year effects; state-and-year fixed effects |
| Robustness | D.C. exclusion and winsorization |
| Panel inference | HC1 heteroskedasticity-robust standard errors; normal-approximation p-values |

The [analysis-ready panel](data/state_panel_2022_2025.csv) and [data dictionary](DATA_DICTIONARY.md) accompany the workbook. Its data and model worksheets make the calculations and evidence available for inspection.

## Limits of the analysis

- **Reporting, not incidence.** IC3 complaints are voluntary. Differences can reflect reporting behavior as well as crime, and extreme incidents can influence state averages.
- **States, not individuals.** State-level associations do not establish individual risk or causal effects.
- **Short time span.** Four years provide limited within-state variation.
- **Uncertainty matters.** HC1 standard errors address heteroskedasticity but do not account for within-state serial correlation through state clustering.

Read rankings as comparisons of reported outcomes, not a “safest state” score. Read scenarios as sensitivity exercises, not forecasts.

<details>
<summary><strong>Opening the workbook and troubleshooting</strong></summary>

- **Where are the controls?** Open the downloaded workbook in desktop Excel and use the cream input cells. GitHub images are static previews.
- **Values aren't updating?** Check that Excel calculation is set to Automatic, then recalculate.
- **How do I check a scenario?** Set the income change to 0%; model-implied losses should match the selected baseline.
- **Want to inspect the evidence?** Start with `Panel Data`, `Panel Models`, and `Sources & Notes`. See the [reader test checklist](PUBLISHING_GUIDE.md#test-the-reader-experience) for a fuller walkthrough.

</details>

## Sources

- [FBI Internet Crime Complaint Center annual reports](https://www.ic3.gov/AnnualReport/Reports)
- [U.S. Census Bureau American Community Survey](https://www.census.gov/programs-surveys/acs)

Report and data links are also recorded in the workbook.

## Cite this project

Patel, Om. *Scam Geography: The Economics of Reported Internet Crime Across U.S. States, 2022–2025*. Interactive Excel research project. [GitHub repository](https://github.com/Opatel23/scam-geography).

Include the commit SHA or release tag and your access date when citing a particular version. Cite the underlying data sources separately when using their data.

---

**Skills demonstrated:** Excel · data visualization · economic decomposition · panel data · regression · fixed effects · robustness analysis

[Back to top](#scam-geography)
