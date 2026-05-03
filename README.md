### What is being studied?
There is a common belief that it often rains on Midsummer Day (June 23). The question is whether June 23 is simply one of many rainy days or if it stands out in terms of precipitation probability.
The goal is to use historical precipitation data to:

- determine the baseline probability of rain for a random June day 
- estimate the probability of rain on June 23 and compare it to the baseline 
- analyze how precipitation probabilities for all June dates are distributed and whether any date (e.g. June 23) stands out 

### Data
Estonian Environment Agency. Estonian Weather Service: https://www.ilmateenistus.ee/kliima/ajaloolised-ilmaandmed/
Dataset: Tallinn-Harku 2004–2025, hourly observations (Excel). The data is converted to CSV and summed up into daily totals.

### Methodology
For Data preparation I check column names, data types, and missing values. Combine the datasets, extract precipitation data, and create a unified CSV file for analysis. Filter June data and sum hourly precipitation into daily totals.

To understand the data, I first examine June 23 across years. The variability is high: most years have little or no precipitation, while some years have very high values. Based on this, I define thresholds: >0 mm (light rain), >5 mm (moderate rain), >10 mm (heavy rain). 

Probabilities are calculated as frequencies. The dataset includes 22 years of daily observations: baseline is calculated from 660 observations; each date-specific probability is based on 22 observations. Results are visualized on plots.

### Results
June 23 has a slightly higher precipitation probability than the overall June baseline across all thresholds.
<img src="Figures/jaanipaev_vs_juuni.png" width="400">

The difference is most noticeable for heavy precipitation (>10 mm). June 23 belongs to the group of days with higher precipitation probability but does not stand out within that group.

<img src="Figures/tugev_sadu_paevade_loikes.png" width="600">

Since date-specific probabilities are based on only 22 observations, the estimates are subject to higher uncertainty. In addition, the perceived impact of rainfall on June 23 depends not only on daily totals but also on the timing and distribution of precipitation within the day.

### How to run the notebook
Open Ilmaandmed_Clean.ipynb in Jupyter Notebook or JupyterLab and run all cells. The analysis is performed in Python (Anaconda, Jupyter Notebook).
Required libraries: pandas, numpy, matplotlib.

### Further development
Data was downloaded manually from the Ilmateenistus website and converted to CSV. The service also provides partial API access, which could be used for automated data ingestion.

Data cleaning and preparation were performed step by step during the analysis and are documented in the file Ilmaandmed_draft.ipynb.  This could be further developed into a fully automated workflow.

The current solution is built for a specific weather station and time period. It could be generalized using functions to support multiple stations and periods.

### Use of AI
AI was used to assist with Python/pandas/matplotlib questions, code structure, and guidance on GitHub and README preparation.
