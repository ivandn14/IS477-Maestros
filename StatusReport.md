# Interim Status Report

## Work

Up until this point, we have completed the legwork that will allow us to further analyze. We began by pulling our datasets together in our repository and combining their metadata, which was originally split across two files, into a single standardised file. We then performed preliminary data cleaning on each individual dataset, which included removing empty and unnecessary rows, creating and repositioning a proper header row, resetting the index, converting years into clean numerals, and dropping unnecessary columns such as country code, indicator name, and indicator code. We also identified many instances of countries grouped together in the data that had no available values under those groupings and removed them accordingly.

Before merging the datasets, we needed to reformat them. The rows had previously been labelled as countries and the columns as years, so we melted the datasets to flip this structure for easier analysis. One dataset, our second debt-to-GDP dataset, was formatted differently from the other World Bank datasets, so we adjusted it to align with the rest. After merging, we found that many countries lacked data prior to 1990 and that GDP PPP (Gross Domestic Product at Purchasing Power Parity) data were entirely absent before that year, so we removed all pre-1990 entries. To finalize our cleaning, we dropped any entries missing an interest rate, debt-to-GDP rate, or inflation rate, as all three are required to answer our research question.

Following the cleaning process, we moved into analyzing the data. We computed GDP growth as a derived variable by calculating the year-over-year percent change in real GDP for each country, with extreme outliers capped at plus or minus 50 percent. Countries were then classified into four debt-to-GDP tiers — low (below 40%), medium (40%–80%), high (80%–120%), and very high (above 120%) — which serve as the primary grouping variable across all visualisations. From there, we generated four charts: a scatter plot of real interest rate levels versus inflation rate by debt tier, a scatter plot of real interest rate levels versus GDP growth by debt tier, a box plot showing the distribution of inflation rates across tiers, and a bar chart of average GDP growth by tier. A summary statistics table was also produced, capturing average interest rates, average and standard deviation of inflation, average GDP growth, and average market capitalization for each tier.

**Repository Artifacts:**
- [Project Notebook](https://github.com/ivandn14/IS477-Maestros/blob/main/IS477Project/IS477_Project.ipynb)
- [Real Interest Rate Dataset](https://github.com/ivandn14/IS477-Maestros/blob/main/IS477Project/Real%20Interest%20Rate%20Dataset.csv)
- [Real GDP Dataset](https://github.com/ivandn14/IS477-Maestros/blob/main/IS477Project/Real%20GDP%20Dataset.csv)
- [Inflation Dataset](https://github.com/ivandn14/IS477-Maestros/blob/main/IS477Project/Inflation%20Dataset.csv)
- [Debt-to-GDP Dataset](https://github.com/ivandn14/IS477-Maestros/blob/main/IS477Project/Debt-to-GDP%20Dataset.csv)
- [Debt-to-GDP Dataset 2](https://github.com/ivandn14/IS477-Maestros/blob/main/IS477Project/Debt-to-GDP%20Dataset2.csv)
- [Market Cap Dataset](https://github.com/ivandn14/IS477-Maestros/blob/main/IS477Project/Market%20Cap%20Dataset.csv)
- [GDP PPP Dataset](https://github.com/ivandn14/IS477-Maestros/blob/main/IS477Project/GDP%20PPP%20Dataset.csv)
- [GDP PPP per Capita Dataset](https://github.com/ivandn14/IS477-Maestros/blob/main/IS477Project/GDP%20PPP%20per%20capita%20Dataset.csv)


## Updated Timeline

The project is on track for the final submission deadline, with minimal deviation from the original plan. All data collection, cleaning, and merging tasks have been completed, and we are currently mid-way through the analysis phase. At this point, we have implemented debt-to-GDP tier classifications and computed GDP growth rates from the raw GDP data. We examined the general relationship between macroeconomic variables and interest rate levels, providing a broad view of how GDP growth, inflation, and other indicators behave at different interest rates.

We need to proceed by investigating how these variables react to year-over-year interest rate changes. Another split that will help our analysis is categorizing countries as developed, developing, and undeveloped based on GDP per capita. This is beneficial because interest rate changes impact countries' economies differently. We will also split the timeframe of 1990–2024 into 5-year periods to observe more granular trends. We have some visualizations that are working, and we expect to have the full visualization suite completed by the week of April 21st.

From there, the remaining work involves interpreting the trends we observe, refining our research questions based on what the data shows, and writing up the final report. While our current work has been done to answer our main research question, we will have to do supplementary work to answer our two other minor questions. We have allocated the weeks of April 21st through April 28th for analysis and interpretation, leaving the final week before the deadline for writing, review, and submission.

---
## Project Changes: 
Due to positive feedback, we did not diverge from the main aspects of the project, but certain details were added. Instead of analyzing Real GDP as initially intended, we switched to Real GDP PPP, as when we analyze countries in separate categories, such as developed, developing, and undeveloped, PPP more accurately shows the standard of living in a nation than regular GDP does. We also decided to exclude data before 1990, because data before then would not represent a modern economy as well as more recent data. Also, breaking countries into tiers based on GDP PPP per capita and splitting our data into 5-year periods are new improvements.

## Challenges: 
One of the more significant challenges we encountered was dealing with missing data. The World Bank datasets use zero as a placeholder for missing values rather than leaving cells empty. This meant that after merging, a large number of entries appeared to have data when they were actually empty, which would have skewed calculations such as averages and standard deviations. We resolved this by replacing all zero values with NaN after the merge, and then dropping any rows that were missing values for our three core variables — interest rate, debt-to-GDP, and inflation rate.

A related issue was that the two debt-to-GDP datasets we sourced were formatted differently from one another and from the rest of the World Bank datasets. The second dataset had a different column structure and used "no data" as a placeholder rather than leaving cells empty. We resolved this by manually reformatting the second dataset to match the structure of the others, replacing "no data" strings with zeros before converting to NaN, and then merging the two debt-to-GDP sources by averaging their values where both were available.

A technical issue also arose when generating the inflation distribution box plot, where the pandas boxplot() function did not support the order parameter needed to display the debt tiers in the correct sequence. This was resolved by switching to the seaborn boxplot() function, which supports tier ordering natively. In regards to our python code, I performed the initial data cleaning on the individual datasets. I purged useless columns and rows, and then flipped them. I then merged them into the one dataset. After merging, I merged two duplicate rows, and deleted some other data. I also worked conceptually, thinking of ways to better analyze the data, such as splitting our inspection into 5-year periods, along with collaborating to change our GDP data to GDP PPP.

## Summary of Contributions

### Nicholas McClintock
	In regards to our python code, I performed the initial data cleaning on the individual datasets. I purged useless columns and rows, and then flipped them. I then merged them into the one dataset. After merging, I merged two duplicate rows, and deleted some other data. I also worked conceptually, thinking of ways to better analyze the data, such as splitting our inspection into 5-year periods, along with collaborating to change our GDP data to GDP PPP.
  
### Ivan Dong

My contributions for this milestone were focused on the analysis phase of the project. I incorporated the GDP PPP per capita dataset into the merged dataframe. Additionally, I provided some slight adjustments to the cleaning code, replacing the zero-filled missing values with NaN to prevent them from skewing calculations. Furthermore, I computed GDP growth rate as a derived variable and classified countries into four debt-to-GDP tiers. Finally, I produced four visualizations to compare interest rate levels to inflation and GDP across debt tiers, as well as a statistics table capturing key metrics for each tier.
