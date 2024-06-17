# Examining Determinants of Opioid Mortality
## Introduction
According to most sources, the "Opioid Epidemic" got its start around the early 1990s and gained traction in the mid-1990s. Opioid drugs are meant to be prescribed to people dealing with severe and chronic pain. Despite its effectiveness as a painkiller, it is a highly addictive substance. The terms "Opioid Epidemic" and "Opioid Crisis" were termed because of the drastic increase in opioid-related deaths, including overdoses and suicide. Our team is interested in the determinants of opioid related-mortality rates. We used public datasets to explore this question, looking at regional, demographic, and economic factors. 

## Research Questions
-What demographics are susceptible to higher rates of opioid mortality?

-Is the opioid crisis region/state specific?

-Is there a relationship between poverty and the amount of opioid related-deaths?

-Has access to prescription opioids shaped the current wave of the opioid crisis?

## Data Aquisition

Sourced demographic data from The Home of the US Government's Open Data website: https://catalog.data.gov/dataset/drug-overdose-death-rates-by-drug-type-sex-age-race-and-hispanic-origin-united-states-3f72f

Drug prescription data by state and year from "Data.Medicaid.gov":(https://data.medicaid.gov/datasets?fulltext=State%20Drug%20Utilization%20Data)

Economic Research Service (USDA)**: [USDA Data](https://data.ers.usda.gov/reports.aspx?ID=17826)

Demographic Data from The Home of the US Government's Open Data**: [data.gov](https://data.gov)

CDC Injury Center: https://www.kaggle.com/datasets/craigchilvers/opioids-in-the-us-cdc-drug-overdose-deaths

## Data Exploration and Clean Up
Multiple datasets related to opioid mortality, demographic, socioeconomic and geographic factors were used in this study. All datasets were acquired as .csv files. API keys were not available on the websites where we obtained our data. Once obtained, subsets of the data, pertinent to our research, were isolated (i.e. overall opioid overdose deaths with a focus on synthetic opioids). Once the datasets were filtered to the key subject matter, a variety of line plots, bar plots, and heatmaps were used to visualize different trends ranging from 1991 to 2023.

### Sample Code
The first dataset was broken down to look at the percentage of people living in poverty for individual states. By doing this, the dataframe only shows relevant information.

     *df = df[['state_National', 'total_est_pct2']] df = df.dropna(inplace=False)*
     
To show this information for every state, a heat map was created from the dataframe.

     *fig = px.choropleth(df, locations='Abbreviation', locationmode="USA-states", color='total_est_pct2', scope="usa", color_continuous_scale="YlOrRd", # or any other color scale title=" % of Sates Population in Poverty")*
     *fig.show()*
     
![Opioid Deaths by Drug](https://github.com/NefertitiM/Determinants-of-Opioid-Mortality/blob/main/images/state_poverty_map.png)


## Data Analysis

In order to get a better understanding of the impacts of synthetic opioids to the US population, the line plot below was created to be able to visually compare the overall opioid death rates to the death rates attributed solely to synthetic opioids, including Fentanyl.  As shown, the trends between the 'All Opioids' and the 'Other Synthetics' lines show similar increasing directionality beginning in 2013 on forward.

![Opioid Deaths by Drug](https://github.com/NefertitiM/Determinants-of-Opioid-Mortality/blob/main/Output/rate_by_synth1.png)



To examine the precentage of people in poverty per individual state, a bar graph was generated. To condense the information, this only showed the top 10 states with the highest percentage of poverty. A smiliar bar graph was made, showing the top ten states with the highest opioid-related deaths per 100k people (these graphs can be found in the powerpoint slides and jupyter notebook). The graph below summarizes the two, allowing for a comparison of state poverty and opioid-related deaths.

![Opioid Deaths by Drug](https://github.com/NefertitiM/Determinants-of-Opioid-Mortality/blob/main/images/poverty_vs_deaths.png)



Exploring geographic factors, bar charts showing overdose rates by state for 2013 and 2019 were generated. These showed an increasing trend for overdose rates. A correlation plot on population density and overdose rates, showed population density to be a more strongly correlated factor in 2019 than in 2013. Another correlation plot showed that poverty became less highly correlated in that same time frame (the bar charts and correlation plot for poverty can be found in the slides and jupyter notebook).

![Opioid Deaths by Drug](https://github.com/NefertitiM/Determinants-of-Opioid-Mortality/blob/main/Output/Pop_density2019.png)



Has the prescription of opioid drugs influenced the increase in opioid deaths? Drug prescription data "Data.Medicaid.gov" was used to quantify the amount of 4 prescription opioids (fentanyl, morphine, oxycodone, and hydrocodone), which was delineated by state and year. From 1991 to 2023 there was an increase in fentanyl prescriptions and a less drastic increase in morphine presctiptions. This is shown in a line plot, aggregating data from all 50 states, and heatmaps depicting the changes in prescription rates by state (heatmaps can be located in powerpoint slides and jupyter notebook). 

![Opioid Deaths by Drug](https://github.com/NefertitiM/Determinants-of-Opioid-Mortality/blob/main/Output/Country_Level_Trends_in_Morphine_Prescriptions.png)


## Result Summary
By 2018, the impacts of opiod overdose deaths was more prominent with men than women, with the ratio of death rates of men to women was 2.23.
The three most highly impacted age groups by opiod overdose deaths were, in descending order, 25 to 34 year olds, 35 to 44 year olds, and 45 to 54 year olds with death rates per 100k of 28.1, 27.7, and 23.0, respectively. For perspective, the overall average death rate for 2018 was 14.3.

There was no obvious trend between poverty rates and opioid-related mortality. However, the top ten states with the highest opioid-related deaths aligns with the results seen in the geographic portion of our research.
In addition, correlation could not be found for drug prescription rates and opiod-related death, however the overall trends fits in with the rest of the data. The amount of fentanyl prescribed by health professional increased over the period from 1991 to 2023, leveling off on the same level as oxycodone, hydrocodone and morphine around 2009. For the years 1991 and 1995, little to no fentanyl was being prescribed. This trend of fentanyl, along with a less drastic increase in the prescription of morphine, precedes the rise in opioid-related deaths starting in the early 2000s. Visualizing these trends by state supports the geographic region as being the major determinant of opiod related-deaths. States with the highest prescription rates of fentanyl and morphine overlap with those having high overdose rates in the southwest and northeast.

This shows that in areas with higher desnity the crisis has deteriorated faster, while things have stayed the same in places where it has historically been prevalent in past decades, such as the Appalachias and Southwest.
A time series plot shows that there is a steady increase from 2013 to 2017, but that there was a mild recovery afterward for the states. This data does not include figures from 2020 onwards, omitting the resurgence in opioid deaths following the Covid-19 pandemic.

## Conclusion
The major determinants of opioid related-mortality was geographic region and demographics. While drug prescription and poverty rates were not strong indicators of drug-related deaths, both datasets support geographic region as being the most impactful factor in opioid mortality.

## Limitations & Further Items
One key limitation to the dataset analyzed is that it does not segregate race and ethnicity as its own demographic factor, as it was only included as a subset of either age or gender.  The ability to analyze the data solely on race and ethnicity could provide a separate view that may broaden the understanding of the impacts of opioids on those particular segments of the population.  This provides an opportunity to further understand why the data was organized in this manner and potentially locate a data source that does provide this information for further analysis.

While the trend of drug prescription appears to be a precursor to the opioid death rate, no direct causation can be shown with our data. Further studies would look into which opioids people were dying from (illicit or prescribed).

No overlap was found with the poverty rate and opioid-related deaths, however parsing the data by household income would provide a better opportunity to understand the impacts of finances on death rate.


The CDC dataset doesn’t capture newer data after 2019, especially the Covid 19 pandemic which saw an increase in death rates due to opioid use.


## Further Implications
Overall, the data shows that a male using opioids, especially synthetics such as fentanyl, between the ages of 25 to 44 years old in the US is being more highly susceptible to overdosing as compared to the overall population.

Based on this dataset, the possible link between overprescription of fentanyl and opioid-related mortality should incentivise medical professionals and pharmaceutical scientists to find a less addictive medication for people dealing with chronic and severe pain.
