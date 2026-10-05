# Publication checklist

Scam Geography is an individual economics project by **Om Patel**. Keep the repository private until you have completed the checks below and are ready to publish it.

[Project overview](README.md) · [Data dictionary](DATA_DICTIONARY.md)

## Release hold

The workbook and preview images still use fraud terminology for all-category IC3 internet-crime totals. Update those labels and source notes consistently, regenerate the previews, and retest the workbook before making the repository public.

## Test the reader experience

Download a fresh copy of the workbook from GitHub and open it in desktop Excel. GitHub's workbook page and the PNG previews are not interactive.

| Check | Action | Expected result |
|---|---|---|
| Orientation | Open `Start Here` | The purpose and navigation are understandable without additional explanation. |
| Comparison | In `Interactive Econ Lab`, change the year, both states, and outcome using the cream input cells | Labels, values, and comparisons reflect the selected inputs. |
| Scorecard | Change state and year in `State Scorecard` | The profile, ranks, and interpretation update together. |
| Scenario | In `Scenario Lab`, enter 0% income change | Scenario loss-per-person values equal the selected baseline. |
| Sensitivity | Change income by 10%, then restore the original inputs | Scenario results update; the noncausal interpretation remains visible. |
| Reopening | Save a test copy, close it, and reopen it | The copy retains its selected inputs and opens without repair warnings. |

If results appear unchanged, check that Excel calculation is set to Automatic and recalculate. Do not edit formula cells to force a result. Record any unresolved issue before publishing.

## Review presentation and research claims

- [ ] Your name is consistent across the README and workbook.
- [ ] All six preview images display on GitHub.
- [ ] The workbook download and data links work.
- [ ] The README agrees with the workbook's model estimates and limitations.
- [ ] Reported complaints are not described as all fraud incidents or unique victims.
- [ ] Associations and scenario calculations are not described as causal effects or forecasts.
- [ ] The data dictionary explains units, lagged ACS timing, and rate denominators.
- [ ] No Excel lock files beginning with `~$`, personal files, or credentials are included.
- [ ] You have reviewed permissions for any included third-party material and decided how others may reuse your original work.

Only change repository visibility when you choose to publish. These checks do not change visibility automatically.

## Portfolio copy

**Repository description**

Interactive economics analysis of reported internet crime across U.S. states, 2022–2025.

**Suggested topics**

`economics`, `econometrics`, `excel-dashboard`, `panel-data`, `cybercrime`, `data-visualization`

**Résumé bullet**

Built an interactive Excel research project combining FBI IC3 and Census ACS data into a 204-observation state panel; used economic decomposition, fixed effects, and robustness checks to examine geographic variation in reported internet-crime losses.

**Short introduction**

I built *Scam Geography* to explore how reported internet-crime losses vary across U.S. states. Readers can compare states, examine complaint frequency and loss severity, and test income-change scenarios while seeing the limits of what the data can establish.

## Suggested project citation

Patel, Om. *Scam Geography: The Economics of Reported Internet Crime Across U.S. States, 2022–2025*. Interactive Excel research project. GitHub. https://github.com/Opatel23/scam-geography

For a reproducible citation, append the commit SHA or release tag used and the access date. Cite the underlying FBI IC3 and Census ACS sources separately when using their data; this project citation does not replace those sources.
