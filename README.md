# Fentanyl_Project1
Dataset Used:
https://www.kaggle.com/datasets/craigchilvers/opioids-in-the-us-cdc-drug-overdose-deaths
#Research Question
The question my data set deals with is: How does the opioid crisis break down by geography and region?
I find it a worthwhile area of exploration because the country of the United States is so vast and demographically widespread. It is fascinating to see how different urban and rural environments and states around the country might be decomposed in terms of drug usage and abuse. This dataset allows us to examine exactly this.
#Data Collection
I used the following dataset assembled from the CDC's Injury Center, which contains overdose rates and deaths by state for the timeframe of 2013-2019. This data is conveniently organized and easy to use, which is what drew me to it in addressing my research question. It also contains state information pertaining to its GDP, poverty rate, inequality, and population density. This is useful for comparing overdose rates to other potentially intervening factors. 
https://www.kaggle.com/datasets/craigchilvers/opioids-in-the-us-cdc-drug-overdose-deaths
#Data Exploration and Cleaning
The first step necessary was examining the data and cleaning it for processing into useful graphs or statistical correlation. I renamed several columns which I deemed worthy of being shortened or otherwise. I found several missing entries for the Capitol, Washington D.C., which I proceeded to drop from my analysis. 
##Examples of Code Cleaning
del drug_df['ï»¿State']
drug_df
drug_df.isnull().sum()
drug_df.rename(columns={"State Abbreviation": "State"},inplace=True)
drug_df.rename(columns={'2019 Age-adjusted Rate (per 100000 population)': '2019 OD Rate',
                        '2018 Age-adjusted Rate (per 100000 population)': '2018 OD Rate',
                        '2017 Age-adjusted Rate (per 100000 population)': '2017 OD Rate',
                        '2016 Age-adjusted Rate (per 100000 population)': '2016 OD Rate',
                        '2015 Age-adjusted Rate (per 100000 population)': '2015 OD Rate',
                        '2014 Age-adjusted Rate (per 100000 population)': '2014 OD Rate',
                        '2013 Age-adjusted Rate (per 100000 population)': '2013 OD Rate'},inplace=True)
clean_overdose_df = drug_df.dropna()
transposed_overdose_df = drug_overdose_rates_df.transpose()
#Data Analysis
My analysis comes from the yearly data across the timeframe. I created two bar charts showing OD rates by state for 2013 and 2019, whereby we can compare the difference. The chart reveals that rates have climbed on the whole, indicating that through the years things have gotten worse, and also showing that rates have not declined in relative terms in the places where rates were already high. I did a correlation plot on population density and OD rates as well for both years. This analysis tells us that population density is a more strongly correlated factor in 2019 than it was in 2013. It was also revealed that poverty became less highly correlated in that same time. This shows that in areas with higher desnity the crisis has deteriorated faster, while things have stayed the same in places where it has historically been prevalent in past decades, such as the Appalachias and Southwest.
