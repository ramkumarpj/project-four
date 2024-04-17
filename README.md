## Project Four

For Project 4, you will work with your group to solve, analyze, or visualize a problem using machine learning models (MLM) with the other technologies we’ve learned. Prepare a 15-minute data deep dive or infrastructure review that shows machine learning in the context of what we’ve already learned.

## Background

Team AEJJ is seeking to discover relationships between U.S. Gross Domestic Product (GDP) and overall economic health. Can machine learning predict a recession, with better than 75% accuracy, by analyzing historical GDP data?

## Setting up Agile Project

Assigned Agile workflow using github projects.  We set up the flow of Project Ideation, Project Poposal, Data Fetching, Data Analysis, Building the ML Model, Testing, Documenting and Presentation. These all include Roles, Communication, Collaboration, Milestones, and tracking when and where we are each day for the entire project to ensure that the project is completed.  Workflow can be found here:

https://github.com/users/scottarterbury/projects/3

## Data Sourcing and Analysis

United States Department of Economics Government Site. Bureau of Economic Analysis (BEA).

National Income and Product Accounts Metadata CSV files download. We used the GDP as the main source as it has shown in the past that it has the strongest indicator.

The dataset contained 100 years worth of data.  We filtered the data to include the top 4 indicicators of a recession in the GDP. Some of the data was mising until 1959 so we started there.  Using an anaylsis of top indicators, we weighed 4 parts of the GDP makeup and analyized that.  

The more recent the data, the largest portions that makes up the total GDP, the higher the weight.

We looked at the quarterly data of the past 20 years to breakdown and filter the data using Python and creating easy to read visualizations.

The conclusion of this data showed the top 4 of the indicators is Personal consumption expenditures, Gross private domestic investment, Net exports of goods and services, Government consumption expenditures and gross investment.

To further breakdown the data collection, we show that the Personal Consumption Expenditures (PCE) includes Goods and Services. The GDP contains Gross Private Domestic Investments for Nonresidential and Residential. The Government consumption expenditures and gross investment includes net exports and net imports and the Defense and Nondefense.

## Data Model Implementation

The generally accepted definition of a recession in the U.S., according to Forbes, is when GDP shrinks in two consecutive quarters. A recession involves a significant decline in economic activity that is spread across the economy and lasts more than a few months. Comparing forecasts with their historical antecedents can produce a measure of the probability of a future recession. Taking into account these definitions, we needed to decide on what Machine Learning technology to use.  Machine Learning algorithms are often drawn from statistics, calculus, and linear algebra. 

Using Python, we started with Linear Regression from Scikit-learn. The data we obtained was used to train the model, proccessed using standard scalar, to find the metrics and test we then used the mean squared error (MSE).  This allowed us to define the features to use for the prediction, define the target variable, create and fit the model, obtain the data and then test.

The next Machine Learning Model we used is Support Vector Machines (SVR) from Scikit-learn. This MLM finds the hyperplane that maximally separates the points of one class from those of the other class. It finds the hyperplane that has the largest margin between the points of the two classes. In Python, we inputed our previously filtered data for training and defined the target variable we wanted answered. We created the SVR pipeline in a scalar format. Afterwards we fit the model and then tested the model with an 0.85 accuracy.

We then tested the Ensemble model learning. 
