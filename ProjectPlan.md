# Project Plan

## Overviews
Within Keynesian economics, there is a general consensus that if a central bank decreases interest rates, this is inflationary and expands the economy, while if it increases interest rates, this is deflationary and contracts the economy. However, this relationship becomes less clear when a government incurs high levels of debt. When governments pay interest on a higher principal, more money enters the economy, potentially offsetting the contractionary effects of higher interest rates.

Our research explores whether this economic principle holds true when a nation has higher debt levels.

We will begin compiling our data and combining it into a unified dataset to answer our research question. We will analyze outliers and data gaps and determine how to proceed. Many countries face circumstances that could significantly impact their economies but are not directly related to our research, such as war, natural disasters, and other shocks. These factors will need to be considered during analysis.

Once our data is cleaned, we will analyze three primary indicators:

- GDP growth  
- Inflation  
- Asset class prices  

These will be analyzed in relation to interest rates and grouped by **debt-to-GDP ratio levels**. The trends we observe will be compiled into our final report.

---

## Team

**Team Members**

- Ivan Dong  
- Nicholas McClintock  

Both team members will collaborate on all aspects of the project. Rather than rigidly dividing responsibilities, we will work together throughout the process so that both members maintain a complete understanding of the project.

### Workflow

**Data Collection**
- Collect datasets
- Combine datasets into a unified structure

**Data Cleaning**
- Handle missing values
- Standardize variables and formats

**Data Analysis**
- Statistical analysis of economic indicators

**Visualization**
- Create graphs and visualizations to communicate findings

**Interpretation**
- Collaboratively interpret results and answer research questions

---

## Research Questions

1. How do interest rates impact **GDP growth, inflation, and asset class prices** in countries with varying debt-to-GDP ratios?

2. Do countries with **higher debt-to-GDP ratios** experience more volatile inflation rates over time?

3. How has **government debt-to-GDP evolved globally over time**, and which countries have experienced the largest structural increases in debt levels?

---

## Datasets

We identified suitable datasets from the **World Bank Group**, a highly reputable international organization that provides financial and development assistance to countries worldwide. The World Bank also serves as an observer to the **UN Development Group**, reinforcing its credibility as a data provider.

All datasets are governed by the **Creative Commons Attribution 4.0 license**, which allows use, modification, and redistribution as long as the original source is credited and changes are documented.

Most datasets originate from the **International Monetary Fund (IMF)** and other global statistical agencies.

### Data Coverage

- Time range: **1960 – 2024**
- Developed countries: mostly complete yearly data
- Developing countries: many datasets begin in the **1990s**

All datasets include **country names and yearly values**, allowing us to merge them into a single analytical dataset.

---

## Initial Datasets

**Interest Rates**  
https://data.worldbank.org/indicator/FR.INR.RINR

**GDP (Current US$)**  
https://data.worldbank.org/indicator/NY.GDP.MKTP.CD

**Government Debt to GDP**  
https://data.worldbank.org/indicator/GC.DOD.TOTL.GD.ZS

**Inflation (Consumer Prices)**  
https://data.worldbank.org/indicator/FP.CPI.TOTL.ZG

**Domestic Companies Market Capitalization (% of GDP)**  
https://data.worldbank.org/indicator/CM.MKT.LCAP.GD.ZS

## Timeline

We will begin by downloading the datasets, cleaning and standardizing them, and merging them into a unified format by country and year. Then we will identify missing values, resolve inconsistencies between datasets, and prepare the final dataset for analysis. Then we will generalize visualizations, such as time-series plots, cross-country comparisons, and trend graphs, to illustrate the relationships among interest rates, GDP growth, inflation, and debt levels. After this step, we can identify trends within the dataset, analyze how variables such as interest rates and debt-to-GDP ratios relate to economic outcomes, and interpret the results. Lastly, we need to refine the research questions, review the results, discuss the limitations, and ensure the conclusions are supported.

---

## Constraints

Luckily, given our research objectives and the datasets we are using, there are no pressing legal or ethical restrictions for our project. Due to the World Bank's license for the datasets, we can use anything or everything for research. Also, because the project is economic and doesn’t directly address inequality, there are no privacy concerns or politically incorrect conclusions in the research. All the data is collected from each national government, so there is no better way to present it.

One potential problem is differences in how countries report economic data, which could skew the data. Another potential problem could be in countries with low freedom index scores, as they may experience false reporting. As mentioned before, most countries’ data begin only in the 1990s, with only a handful spanning back to the 1960s. We can either search for data from the same sources as the dataset to fill the gaps or cap off the time period we are studying. Apart from the missing early data, there is a clear yearly value assigned to each country, which simplifies our data, but could miss fluctuations within the year.

---

## Gaps

### Correlation vs Causation

Our datasets allow us to observe correlations rather than causal relationships. While we are able to identify trends between interest rates, GDP growth, inflation, and asset market size across countries with different debt-to-GDP ratios, the data alone does not prove that interest changes directly cause those outcomes.

### Unexplained Macroeconomic Variables

Many important economic variables that influence GDP growth, inflation, and financial markets are not included in our current datasets. Factors such as government spending, unemployment, exchange rates, and demographic changes can influence economic outcomes. Because these variables are not accounted for, they may affect trends we observe and introduce omitted variable bias.

### Difference Between Countries

Countries have different economic structures and policies, which may influence how interest rates affect their economies. Our analysis averages across these differences, which could mask important country-specific dynamics.

### Time Lag Effects of Monetary Policy

Changes in interest rates typically take months or years to affect economic outcomes such as inflation and GDP growth. Our datasets are organized by yearly observations, which makes it difficult to capture timing of these effects.

### Data Completeness and Reporting Differences

While the World Bank datasets are reliable, there may still be gaps in reporting across countries. Some developing countries have limited historical data or have a reporting start date later than others. This could affect the comparability of data across countries.
