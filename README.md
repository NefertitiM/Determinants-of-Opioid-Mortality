# Examining Determinants of Opioid Mortality
## Introduction
### According to most sources, the "Opioid Epidemic" got its start around the early 1990s and gained traction in the mid-1990s. Opioid drugs are meant to be prescribed to people dealing with severe and chronic pain. Despite its effectiveness as a painkiller, it is a highly addictive substance. The terms "Opioid Epidemic" and "Opioid Crisis" were termed because of the drastic increase in opioid-related deaths, including overdoses and suicide. Our team is interested in the determinants of opioid related-mortality rates. We used public datasets to explore this question, looking at regional, demographic, and economic factors. 
## Research Questions
### -How much have fentanyl and other synthetic opiods driven overall opiod overdose deaths in the most recent past?
### -Have certain demographic groups been affected more than others?
### -Is the opioid crisis region specific?
### -Does poverty influence opioid mortality rates?
### -Has access to prescription opioids shaped the current wave of the opioid crisis?
### -What demographics are susceptible to higher rates of opioid mortality?

## Data Aquisition
### -Sourced demographic data from The Home of the US Government's Open Data website (https://data.gov)
### -"Data.Medicaid.gov" (https://data.medicaid.gov/datasets?fulltext=State%20Drug%20Utilization%20Data)
>Data showing drug prescription, and medical reimbursements by state and year were downloaded as csv files.
###
## Data Exploration and Clean Up
### Once obtained, the process for the demographic data set involved understanding the figures being presented (i.e. number of overdose deaths per 100,000 individuals per calendar year) and isolating the subsets of data that were pertinent to our research (i.e. overall opioid overdose deaths with a focus on synthetic opioids). Once the dataset was focused on our key subject matter, the readily available demographic data, of gender and age groups, was parsed out to isolate each demographic subgroup in order to visually present the trends from the years of 1999 through 2018.
### A similar process was used to produce a visualization of the impact of fentanyl and other synthetic opiods as compared to all opiods.
###
### For the "Data.Medicaid.gov", multiple datasets were used, cooresponding to their year (ex."State Drug Utilization Data 20XX").The individual datasets were first filtered on the website because the csv files were very large. They were filtered for drug name and suppression status (whether or not the data was protected/availible). Once added to the local repository and loaded/read on jupyter notebook, relevant columns were filtered for the dataframes (drug name, state, medicaid reimbursements,...etc). Basic statistics were performed on the data to get the average values and then those values were plotted in line plots and heatmaps (ex.Fentanyl Prescription Rates per Capita...). Regression analysis was also done and printed onto the plots.
## Data Analysis
### For the "Data.Medicaid.gov", basic statistics were performed on the data to get the average values and then those values were plotted in line plots and heatmaps (ex.Fentanyl Prescription Rates per Capita...). Regression analysis was also done and printed onto the plots.

###
###
###
## Result Summary
### By 2018, the impacts of opiod overdose deaths was more prominent with men than women, with the ratio of death rates of men to women was 2.23.
### The three most highly impacted age groups by opiod overdose deaths were, in descending order, 25 to 34 year olds, 35 to 44 year olds, and 45 to 54 year olds with death rates per 100k of 28.1, 27.7, and 23.0, respectively. For perspective, the overall average death rate for 2018 was 14.3.
###
### The amount of fentanyl prescribed by health professional increased over the period from 1991 to 2023, leveling off on the same level as oxycodone, hydrocodone and morphine around 2009. For the years 1991 and 1995, little to no fentanyl was being prescribed.
### 
###
## Conclusion
### The prescription of the synthetic drug fentanyl did increase from 1991 to 2023, overlapping with the timeline for opioid-related drug deaths increasing. One possiblility is that the increase in fentanyl prescription preceeded and influenced the later increase in mortality rates. However, to definitvly say that increased fentanyl prescription contributed to the opioid epidemic, we would need data showing which drugs, prescribed or illicit, are driving the opioid-related deaths.
###
## Further Implications
### Overall, the data shows that a male using opioids, especially synthetics such as fentanyl, between the ages of 25 to 44 years old in the US is being more highly susceptible to overdosing as compared to the overall population.

### Based on this dataset, the possible link between overprescription of fentanyl and opioid-related mortality should incentivise medical professionals and pharmaceutical scientists to find a less addictive medication for people dealing with chronic and severe pain.