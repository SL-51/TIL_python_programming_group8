## Repository Group 8 - README file
**Authors**

- S.J. (Sem) Boonstra
- S. (Stefanos) Demenegas
- S. (Seongje) Lee
- M.T. (Mika) Schuback
- T.M. (Teodros) Semma

**Date:** 06.11.2026

**Branch explanation** 

This repository contains the following folders:
- **Data/**: Contains all downloaded datasets used in the analysis (see more in the "Datasets" section).
- **Images/**: Contains all output figures from the analysis and used in the final report.

The root directory also contain the following files:
- **final_notebook.ipynb**: The final report in Jupyter Notebook format.
- **group8_project_proposal.ipynb**: The project proposal.
- **project_group8.py**: The complete Python script containing the data preparation, analysis and visualation pipeline. It is well structured using comments and functions and includes all code used.
- **README.md**: This file, providing project information and instructions for reproducing the analysis.

**Data Analysis Pipeline**

In order to reproduce the analysis and generate the outputs presented in the final report:
1. Clone or download the repository.
2. Ensure that Python and all required packages listed below are installed.
3. Make sure that the original datasets are available in the Data/ folder.
4. Open and run project_group8.py from the repositoriy's root directory.

The script reads the datasets, performs the data preparation and analysis and generates the corresponding figures. The script should be executed from the repository's root directory to ensure that the relative paths work correctly

**Required Packages**

The following Python packages are required:
- numpy
- pandas
- matplotlib
- plotly
- pycountry
- statsmodels
- openpyxl

The os and matplotlib.dates modules are included with Python and Matplotlib, respectively, and do not require separate installation.

**Datasets**

All data is publicly available and standardized across EU countries. The analysis uses quarterly data from 2006 to 2025. 
Rail passenger demand is expressed per inhabitant to account for differences in country size and population changes. Since population is only available annually, the same value is used for all four quarters of a year. 
Fuel prices are converted to real prices by dividing by the general price index so that long-term inflation does not distort the comparison.
The datasets used are summarised below:

| Variable | Measure | Source | Frequency |
| --- | --- | --- | --- |
| Rail passenger demand | 1000 passengers (table rail_pa_quartal) | [Eurostat](https://ec.europa.eu/eurostat/databrowser/view/rail_pa_quartal__custom_22991950/default/table) | Quarterly |
| Population | Population on 1 January (table demo_pjan) | [Eurostat](https://ec.europa.eu/eurostat/databrowser/view/demo_pjan__custom_22992121/default/table) | Annual |
| Fuel prices | Petrol and diesel pump prices incl. taxes | [EU Weekly Oil Bulletin](https://energy.ec.europa.eu/data-and-analysis/weekly-oil-bulletin_en#price-developments) | Weekly |
| General inflation | HICP, all-items index (2025=100) | [Eurostat](https://ec.europa.eu/eurostat/databrowser/view/prc_hicp_minr__custom_24165723/default/table) | Monthly |

Weekly fuel prices and monthly HICP observations are aggregated into quarterly averages for consistency with the rail passenger demand data.