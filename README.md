## Project Four

For Project 4, you will work with your group to solve, analyze, or visualize a problem using machine learning (ML) with the other technologies we’ve learned. Prepare a 15-minute data deep dive or infrastructure review that shows machine learning in the context of what we’ve already learned.

## Background

Team AEJJ is seeking to discover relationships between U.S. Gross Domestic Product (GDP) and overall economic health. Can machine learning predict a recession, with better than 75% accuracy, by analyzing historical GDP data?

## Data Sourcing

United States Department of Economics Government Site. Bureau of Economic Analysis (BEA).

National Income and Product Accounts Metadata CSV files download. We used the GDP as the main source as it has shown in the past that it has the strongest indicator.

The dataset contained 100 years worth of data.  We filtered the data to include the top 4 indicicators of a recession in the GDP. Some of the data was mising until 1959 so we started there.  Using an anaylsis of top indicators, we weighed 4 parts of the GDP makeup and analyized that.  

The more recent the data, the largest portions that makes up the total GDP, the higher the weight.

We looked at the quarterly data of the past 20 years to breakdown and filter the data using Python and creating easy to read visualizations.

The conclusion of this data showed the top 4 of the indicators is Personal consumption expenditures, Gross private domestic investment, Net exports of goods and services, Government consumption expenditures and gross investment.

To further breakdown the data collection, we show that the Personal Consumption Expenditures (PCE) includes Goods and Services. The GDP contains Gross Private Domestic Investments for Nonresidential and Residential. The Government consumption expenditures and gross investment includes net exports and net imports and the Defense and Nondefense.
