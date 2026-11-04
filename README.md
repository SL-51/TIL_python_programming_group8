## Repository Group 8 README file
**Authors**

- S.J. (Sem) Boonstra
- S. (Stefanos) Demenegas
- S. (Seongje) Lee
- M.T. (Mika) Schuback
- T.M. (Teodros) Semma

**Date:** 06.11.2026

**Branch explanation** 

The main branch of the repository contains the following folders:
- Data: It has all the downloaded datafiles (see more in section "datasets")
- Images: All the output images from the code that are used in the final report

Then in the main folder there are also the following separate files:
- final notebook: The final report in notebook format
- group8_project_proposal: The project proposal
- project_group8: The complete code for the whole assignment. It is well structured using comments and functions and includes all code used.
- This README file

**Pipeline**

1. Install all neccesary packages
2. 

**Packages (to be installed)**

- Numpy
- Pandas
- matplotlib.pyplot
- plotly.graph_objects
- plotly.io
- plotly.express
- pycountry
- statsmodels.formula.api
- os
- matplotlib.dates

**Datasets**

All data is publicly available and standardized across EU countries. The analysis uses quarterly data from 2006 to 2025. Rail passenger demand is expressed per inhabitant to account for differences in country size and population changes. Since population is only available annually, the same value is used for all four quarters of a year. Fuel prices are converted to real prices by dividing by the general price index so that long-term inflation does not distort the comparison.

| Variable | Measure | Source | Frequency |
| --- | --- | --- | --- |
| Rail passenger demand | 1000 passengers (table rail_pa_quartal) | [Eurostat](https://ec.europa.eu/eurostat/databrowser/view/rail_pa_quartal__custom_22991950/default/table) | Quarterly |
| Population | Population on 1 January (table demo_pjan) | [Eurostat](https://ec.europa.eu/eurostat/databrowser/view/demo_pjan__custom_22992121/default/table) | Annual |
| Fuel prices | Petrol and diesel pump prices incl. taxes | [EU Weekly Oil Bulletin](https://energy.ec.europa.eu/data-and-analysis/weekly-oil-bulletin_en#price-developments) | Weekly (averaged to quarters) |
| General inflation | HICP all items | [Eurostat](https://ec.europa.eu/eurostat/databrowser/view/prc_hicp_minr__custom_22993037/default/table) | Monthly (averaged to quarters) |
