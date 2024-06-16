# Fentanyl_Project1


# Analysis of Poverty and Opioid-Related Deaths in the United States

## Question and Motivation

**Question:** Is there a relation between people in the United States that live in poverty and the amount of deaths related to opioids?

I find this question interesting because I believe that there is an assumption that people who live in poverty are more likely to be using and/or dying from the opioid crisis that is going on in the United States. I wanted to find out if that assumption were true.

## Data Collection and Research

To further dive into the question above, I needed to find various datasets that could help me find my answer. I first decided that I wanted to look at each state individually and find out the percent of each state's population that lived in poverty.

After finding that data, I determined that if I wanted to see if there was a relation between people in poverty and deaths related to opioids, I needed to find a second dataset that would show me the number of deaths in each state that were due to opioids.

### Data Sources

1. **Economic Research Service (USDA)**: [USDA Data](https://data.ers.usda.gov/reports.aspx?ID=17826)
2. **Demographic Data from The Home of the US Government's Open Data**: [data.gov](https://data.gov)

## Data Exploration and Clean-Up Process

Once I had my datasets, each dataset included plenty of information that was unrelated to what was important to me. I needed to make sure I was only looking at the necessary information related to my question. I broke down the first dataset to look only at the individual state itself and the percent of each state's population that lived in poverty.

### Code Example for Cleaning Poverty Data

```python
df = df[['state_National', 'total_est_pct2']]
df = df.dropna(inplace=False)









