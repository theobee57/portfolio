# My Data Science Portfolio

I am an experienced Information Technologist with a passion for data science. I love data science because it is a key driver of the AI revolution, transforming our world, identifying needs, opportunities, and areas for improvement. I am a Data Analyst, working my way up to becoming a Data Scientist.

## Education
- BSc (Honours) Information Systems in Computer Science and Information Systems, University of South Africa
- Certificate in Oracle E-Commerce Development, University of Toronto
- Certificate in Project Leadership (Postgraduate) in Project Management, University of Waterloo 

## Data Science credentials:
- Data Analyst (Python), DataCamp
- Data Analyst Associate (SQL), DataCamp
- Associate Data Scientist, DataCamp (to be completed soon)

## Data Science Courses completed:
### Python
- Introduction to Python
- Intermediate Python
- Data Manipulation with Pandas
- Joining Data With Pandas
- Introduction to Statistics in Python
- Introduction to Data Visualization With Matplotlib
- Introduction to Data Visualization With Seaborn
- Introduction to Functions in Python
- Python Toolbox 
- Exploratory Data Analysis in Python
- Working With Categorical Data in Python
- Data Communication Concepts
- Introduction to Importing Data in Python
- Cleaning Data in Python
- Working With Dates and Times in Python
- Writing Functions in Python
- Introduction to Regression With Statsmodels in Python
- Sampling in Python
- Hypothesis Testing in Python
- Experimental Design in Python
- Supervised Learning with Scikit-Learn
- Unsupervised Learning in Python
- Machine Learning With Tree-based Models in Python

### SQL
- Joining Data in SQL
- Data Manipulation in SQL
- Exploratory Data Analysis in SQL
- PostgreSQL Summary Stats and Window Function
- Data-Driven Decision Making in SQL
- Applying SQL to Real-World Problems

## My Latest Projects
===========================================
## Revenue Health & Churn Risk Simulator (Executive Decision Support)
![Revenue Health/Risk](/images/dashboard1.png)   
### Tools

Tableau Desktop · Parameters & Actions · Calculated Fields

Dataset: IBM Telco Client 

### 1. Business Background

The business uses a subscription model with multiple contract types and customer segments. While revenue appears steady, leadership faces an ongoing challenge:

How much revenue is exposed to churn risk, and how sensitive is that risk to leadership’s tolerance level?

Traditional dashboards report churn and revenue separately. This project closes that gap, enabling executives to simulate risk tolerance decisions and immediately see their impact on revenue exposure.

### 2. Business Objectives

This project supports executive decision-making by answering the following questions:

* How concentrated is revenue across contract types?
* Which segments exceed acceptable churn risk?
* How does revenue exposure change as churn tolerance tightens or loosens?
* Where should retention efforts be given priority to protect revenue?

### 3. Data Overview

The dataset contains customer-level subscription data, including:

* Monthly charges (revenue proxy)
* Customer tenure (lifecycle indicator)
* Contract type
* Internet service type
* Customer churn status (Yes/No)

Because the dataset lacks calendar-based snapshots, all metrics were defined to ensure accuracy, transparency, and defensibility.

### 4. Key Metrics Defined

Active Monthly Revenue

Sum of monthly charges for non-churned customers.

Used as a proxy for Monthly Recurring Revenue (MRR).

Active Customers

Distinct count of customers who have not churned.

Customer Churn Rate

Proportion of customers who have discontinued within each segment.

Note: Monthly churn was intentionally avoided due to data limitations.

Revenue at High Churn Risk (Executive KPI)

Revenue associated with segments whose churn rate exceeds a user-defined risk threshold.

### 5. Analytical Approach

This project goes beyond descriptive analytics by introducing parameter-driven what-if analysis.

Key design principles:

* Metrics remain stable and validated.
* Parameters control analytical logic, not data filtering.
* Executives define what “high risk” means.
* The dashboard responds instantly without recalculating base metrics.

### 6. Dashboard Design

## Key Business KPIs with Risk Exposure
In addition to core revenue and churn metrics, this dashboard quantifies how much revenue is exposed to churn risk above a configurable tolerance level.
![KPIs](/images/KPIs2.png)
A dedicated KPI row provides immediate business context:

* Active Monthly Revenue
* Active Customers
* Overall Customer Churn Rate
* Revenue at High Churn Risk (dynamic)

Together, these KPIs answer:

“How large is the business, and how much of it is at risk?”

Core Analytical Views

Revenue Contribution by Contract

Highlights revenue concentration across contract types, showing which segments are most critical to business stability.

Customer Churn Risk by Contract

Uses parameter-driven coloring to classify contract types as acceptable risk or high risk, based on executive-defined thresholds.

Monthly Charges vs Customer Tenure

Provides diagnostic insight into the relationship between customer tenure and revenue contribution.

### 7. Key Insights

* Revenue is heavily concentrated in longer-term contracts, creating both strength and dependency.
* Month-to-month contracts consistently exhibit churn rates above typical risk tolerance levels.
* As churn risk thresholds tighten, a disproportionate share of revenue becomes classified as “at risk.”
* Revenue exposure is more sensitive to churn tolerance decisions than to changes in total customer count.

### 8. Recommendations

Based on the analysis:

1. Protect high-value segments
2. Prioritize retention strategies for long-term contract customers who contribute the majority of revenue.
3. Reduce exposure in high-risk segments.
4. Introduce targeted incentives or contract migration strategies for month-to-month customers.
5. Use risk tolerance explicitly.
6. Leadership should align churn risk thresholds with the business strategy, while being aware of the trade-off between growth flexibility and revenue consistency.

### 9. Why This Project Matters

This project shows my ability to:

* Design executive-focused KPIs
* Use parameters for scenario simulation, not gimmicks.
* Translate analytical metrics into risk-based decision support.
* Balance technical correctness with business usability.

Instead of reporting churn and revenue independently, this dashboard connects them to inform leadership action.

### 10. What I’d Explore Next

With additional data, I would extend this analysis by:

* Modeling churn risk by tenure cohorts
* Quantifying the cost of churn-mitigation strategies
* Simulating revenue impact of contract-mix changes
* Integrating time-based churn snapshots for trend analysis

### Final Note

This project demonstrates how I approach executive analytics problems:

clear metric definitions, validated logic, and interactive tools that support real decisions instead of static reporting.

​





========================================

## New Product Sales Strategy
![Sales Strategies](/images/sales_strategies.png)       

The project had two main objectives:
- Determine the optimal sales strategy for a new product launch
- Establish a metric to evaluate sales revenue

My initial step was to perform a thorough cleaning and validation of raw data to ensure data integrity. I did that by using Pandas to check for correct data types, missing values, and other quality issues across all fields.

For exploratory data analysis, I utilized visualization tools from the Matplotlib and Seaborn packages along with Python and Pandas.

I used boxplots to compare performance across different strategies, line graphs to identify revenue trends over a six-week product launch, and heatmaps to determine the correlations between revenue and other factors.

My analysis identified email campaigns as the most effective sales strategy. Based on this finding, I recommended using "Average Revenue per Email Customer" as a metric to monitor revenue. Then, I established a baseline value for this metric.

At the end of the project, I formally communicated my findings and recommendations with a 10-minute presentation, which I delivered to sales representatives, providing them with a clear understanding of the project's insights and recommendations.

I showed how my recommendation directly impacts the business by increasing revenue by 40%.

## Predictive Modeling for Agriculture
The objective ot the project was to determine which soil feature (nitrogen ('N'), phosphorus ('P'), potassium ('K'), or pH) serves as the best predictor of crop type.

My first step involved thoroughly cleaning and validating the raw data to ensure its integrity. I accomplished this using Pandas, checking for correct data types, missing values, and other quality issues across all fields.

Next, I imported the necessary functions from the scikit-learn package, including LogisticRegression, train_test_split, and metrics.

Holding the dataset in a Pandas DataFrame, I organized the data into features and the target variable, which is the crop type.

I used the train_test_split function to divide the dataset into training and testing sets.

For each feature ('N', 'P', 'K', and pH), I trained a logistic regression model and calculated the F1 score. Finally, I compared the F1 scores to identify the best predictor.

My analysis offered valuable insights for agricultural planning, assisting farmers in selecting the most appropriate crops to cultivate.

## Employee Analytics: Preparing Data for Modelling
The project's objectives were to
 Prepare the raw employee data for analytical tasks by ensuring that each column has the correct data type 
filter the dataset according to a given subset of interest.

The focus of this project was on data type conversion. I systematically converted columns to more appropriate data types to ensure proper handling. Numerical columns, such as "Employee ID" and "Training Hours," were converted to either int32 or float16 as needed. 

Also, categorical columns, like gender and department, were transformed into the category data type.

For columns with a natural order (e.g., Small, Medium, Large), I explicitly defined the order of categories using cat.set_categories.

For columns that represent binary choices, I renamed them to be more descriptive (True/False) and then converted them to the Boolean data type.

To prevent altering the original data, I worked with a copy stored in a Pandas dataframe.

After finishing the data type conversion, I filtered the dataframe based on specific criteria that had been established beforehand.

By the end of the project, the dataset contained only the desired subset of data, with each column having the correct data type.

The data was thus ready for both analytical and machine learning tasks.
## Investigating Netflix Movies
![Netflix Movies of the 1990s](/images/Netflix.png) 
The objective of this project was to conduct exploratory data analysis on Netflix data to uncover insights into movies from the 1990s, a pivotal decade in the modern film industry, and provide answers to specific business questions.

I  used Pandas for manipulating the dataset, Matplotlib for visualization, and Python for programming.

Having loaded pre-cleaned Netflix data into a pandas DataFrame, I subsetted the DataFrame to include only movies released between 1990 and 1999.

I then created a histogram based on the 'Duration' column. This visualization enabled me to determine the distribution of movie lengths in that decade, especially the most common movie duration and other insights.

I applied a second filter to isolate the 'Action' genre. Then I iterated through this filtered dataset using a for loop with a counter variable to count each movie that met various duration criteria.

The results had a direct impact on Netflix's content strategy, enhancing user experience and refining its market position.

## New York City Public School Results
The project's objective was to evaluate the performance of New York City public schools and provide policymakers, government officials, parents, and other stakeholders with actionable insights and answers to pertinent questions, especially
- Which schools have the best math results?
- What are the top ten schools based on combined SAT scores?
- What is the distribution of SAT scores by borough?

After importing data from a CSV file, I used Pandas DataFrames to perform a thorough data validation and ensure the dataset was clean and ready for analysis. 

Throughout the project, I employed data visualization tools from the Matplotlib and Seaborn packages to present the findings clearly and highlight significant trends.

To determine the schools with the best math results, I subsetted the DataFrame according to a given metric (math score greater than 80).

To identify the top ten schools, I created a new column in the original DataFrame that represents the total score. This total score is calculated by summing the three existing SAT columns: Math, Reading, and Writing. Next, I sorted the DataFrame by this new column in descending order and selected the top ten rows.

To summarize SAT performance across the various boroughs of New York City, I organized the data by borough and then calculated the count, mean, and standard deviation for each borough.

The project provided answers to the following questions about New York City schools:
- Schools with the best Math results
- The top ten schools based on a combined average of three SAT scores
- The count, mean, and standard deviation of SAT scores by borough

The results of this analysis provided actionable insights that can inform educational policymakers, guide parents in making school choices, and support resource allocation by city planners.

## Visualizing the History of Nobel Prize Winners
In this project, I analyzed a Nobel Prize dataset that contains award information from the inception of the awards in 1901 to 2023. The objective was to answer specific questions about Nobel laureates.

I began by thoroughly cleaning and validating the raw data, checking for appropriate data types, missing values, and other quality issues.

I employed Python programming along with Pandas for data manipulation and Numpy for numerical/statistical operations to find the required answers.

 ### Question 1 - What is the most commonly awarded gender and birth country?

I identified the most common gender among Nobel Prize winners by applying the `value_counts()` method to the "sex" column, sorting the results in descending order. This analysis revealed that the most frequent gender is male. Similarly, I used the same method on the "birth_country" column to determine the most common country, which is the USA.

### Question 2: Which decade had the highest ratio of U.S.-born Nobel Prize winners to total winners across all categories?

I created a Boolean column, "USA_winner", to flag winners from the US. I then made a new column called "decade" by rounding the year down to the nearest decade. 

I organized the data by decade and calculated the average of the USA_winner column, which reflects the proportion of US winners in each decade. Ultimately, I identified that the decade with the highest proportion was the year 2000.

### Question 3: In which decade and Prize category combination was the proportion of female laureates the highest?

I created a Boolean column named "female" to indicate female winners. Next, I grouped the data by both decade and category and calculated the mean proportion of female winners for each unique combination. 

Finally, I identified the combination with the highest mean, which was 2020 in the Literature category.

### Question 4: Who was the first woman to receive a Nobel Prize, and in which category did she win?

I filtered the DataFrame to include only female laureates. After that, I sorted this subset in ascending order by year. Finally, I extracted the full name and category of the first entry in the sorted list to identify Marie Curie and her Physics prize correctly.

### Question 5: Which individuals or organizations have won multiple Nobel Prizes?

I counted the occurrences of each name in the "full_name" column and filtered the results to include only those names that appeared more than once. The following list shows the names that met this criterion:
- Comité international de la Croix-Rouge (International Committee of the Red Cross)
- Linus Carl Pauling
- John Bardeen
- Frederick Sanger
- Marie Curie, née Sklodowska
- Office of the United Nations High Commissioner for Refugees (UNHCR)

## Analyzing Crime in LA
![Crimes Committed in LA](/images/LA_crimes.png) 

The objective of this project was to conduct an exploratory data analysis on a crime dataset to answer three specific questions for the Los Angeles Police Department (LAPD): 

1. Which hour of the day has the highest number of crimes committed?
2. Which area experiences the most nighttime crimes?
3. What is the frequency of crimes across different age groups?

To ensure data integrity, I performed a thorough cleaning and validation of the raw data. I utilized Pandas to verify the correctness of data types, identify missing values, and address other quality issues across all fields.

First, I created a new integer column to store the hour of the day. I then used a Seaborn count plot to visualize the number of crimes occurring during each hour.

To identify the area with the highest number of nighttime crimes, I filtered the dataset to focus on incidents that took place between 10 PM and 4 AM (specifically during the hours 22, 23, 0, 1, 2, and 3). Next, I grouped the filtered data by area name and counted the number of crimes that occurred in each area.

Next, I categorized the "Victim Age" column into predefined age groups using the pd.cut() function. Then, I applied value_counts() to the new "Age Group" column to determine the frequency of crimes within each age category, highlighting the most frequently victimized group.

This project successfully identified patterns in criminal behavior in Los Angeles. The LAPD can utilize the insights (the answers to the three questions)  to allocate resources effectively and address crime in various areas.


## Exploring Airbnb Market Trends
This project had two main objectives: to merge three different Airbnb datasets, each with its own file type and information, and calculate key business metrics based on the consolidated data, which include:
 The average price of room listings
The number of listings categorized as "Private Room"
The most recent review dates for the rooms

I began by loading three datasets: a CSV file containing pricing information, an Excel file with details about room types, and a TSV file that included review dates.

After merging these datasets into a single dataframe using the "listing_id" column as a shared key, I selected the columns that were of interest: "last_review," "room_type," and "price."

To clean the data, I made several changes. First, I converted the price column from a string format (e.g., "140 dollars") to an integer (140) to enable mathematical and statistical operations on this column.

Next, I altered the "last_review_date" column from a string format into a suitable date format using Pandas `to_datetime` function, which allows for date operations on this column.

Also, I standardized the "room_type" column by converting all entries to lowercase, ensuring consistency (for example, changing "Private room" and "private room" to "private room").

As required by the business, I calculated the key metrics and stored them in a dictionary for further analysis.

Due to the high demand for temporary lodging in New York City, the insights gained from this project will help visitors make informed choices among the numerous Airbnb listings available. Besides, Airbnb can use this information to refine its business model.

## Modeling Car Insurance Claim Outcomes
The objective of the project was to analyze an auto insurance dataset to identify the most significant feature, such as driving experience or vehicle type, that predicts whether a customer will file a claim on their policy.

My first step involved thoroughly cleaning and validating raw data to ensure data integrity. I used Pandas to check data types, missing values, and other quality issues across all fields.

I imputed the missing values for the credit_score and annual_mileage columns using the mean of their respective columns.

I used Python to achieve the following tasks programmatically:

1. Trained a univariate logistic regression model for each feature using `statsmodels.formula.api.logit`.
2. Created a confusion matrix based on the model's predictions.
3. Calculated accuracy using the formula (TP + TN) / (TP + TN + FP + FN), and stored the results in a list.
4. Identified the best-performing feature along with its corresponding accuracy from the list.

The project identified the single best predictor of a customer's likelihood of making an auto insurance claim. This insight is invaluable for the project owner.

## Hypothesis Testing With Men's and Women's Soccer Matches
The objective of this project was to test the hypothesis: Women's World Cup matches have more goals than men's World Cup matches.

I loaded two datasets for men's and women's soccer results. I filtered both datasets to include only matches from the FIFA World Cup held after January 1, 2002.

I added a new column named goals_scored to both filtered datasets by summing the home_score and away_score. Additionally, I included a group column to classify matches as either "men's" or "women's".

I created histograms of the goals_scored column for both men's and women's matches to visualize the distribution of goals scored and assess whether the data is normally distributed.

Since the men's and women's matches are independent, and the goals scored are not normally distributed, I conducted a Wilcoxon-Mann-Whitney U test to compare the two groups.

I conducted the test using two different libraries: Pingouin and SciPy.stats, both configured with the parameter alternative= "greater," which establishes a right-tailed test. This tests the specific hypothesis that the median number of goals in women's matches is greater than the median number of goals in men's matches.

I extracted the p-value from the Pingouin test results and compared it to a predefined confidence level of 0.01.

The p-value was less than the confidence level, indicating that the null hypothesis should be rejected.

##  Clustering Antarctic Penguin Species
![Antartic Penguins](/images/penguins.png) 

The objective of this project was to analyze a dataset of Antarctic penguins to categorize them based on their physical features.

To accomplish this, I utilized Python and several key packages: Pandas for data cleaning, validation, and manipulation; StandardScaler from the sklearn.preprocessing library; KMeans from the sklearn.cluster library, and Matplotlib for visualization.

The primary task was to apply K-Means clustering to group penguins based on their physical characteristics. However, I needed to carry out two preprocessing steps before executing the clustering.

First, I converted all categorical columns into numerical format using the `pd.get_dummies` function. This process generated new columns with binary values (0s and 1s) for each category, which is crucial for the K-Means algorithm to function correctly.

Second, I standardized all numerical features using StandardScaler to ensure that no single feature would dominate the clustering process due to its larger magnitude.

After preprocessing the data, I applied the "Elbow Method" to determine the optimal number of clusters (k) within a range from 1 to 9. The resulting plot revealed an "elbow" at k=4, indicating that four clusters is the most suitable choice.

Next, I executed K-Means using four clusters (n_clusters=4), and added the cluster assignments as a new column to the original DataFrame.

Finally, I created a scatter plot to visualize the clusters, showcasing the culmen (beak) length in millimeters for each assigned cluster.

Dr. Kristen Gorman and her research team at Palmer Station in Antarctica will find the results of this project very helpful.

## Predicting Movie Rental Durations 
The goal of this project was to predict the number of days a customer will rent a DVD based on a specific set of features. The project was initiated by a company looking to fill the void left by Netflix’s discontinuation of its DVD-by-mail service in September 2013.

To achieve this, I utilized Python and several essential packages: Pandas, NumPy, "train_test_split" from "sklearn.model_selection", and "mean_squared_error" from "sklearn.metrics".

My overall plan was to compare the performance of two different regression models: a Lasso-based linear regression and a Random Forest Regressor. I aimed to select the model with the lowest Mean Squared Error (MSE) as the best.

To prepare for this task, I derived a new column, "rental_length_days", by subtracting the "rental_date" from the "return_date". Additionally, I created two new binary columns, "deleted_scenes" and "behind_the_scenes", to indicate the presence of these special features.

Next, I defined the target variable y as rental_length_days and established the feature set X  by dropping all irrelevant columns. To finish the prep, I split the data into training and testing sets.

For the Lasso regression model, I wrote a Python program that:
- Trains a Lasso model on the training data.
- Selects only the features with a positive coefficient, effectively removing those that the model determined to be unhelpful.
- Trains an Ordinary Least Squares (OLS) linear regression model using only these selected features.
- Evaluates the OLS model's performance by calculating the MSE on the test set and stores the results.

In the second part of the task, my program built and tuned a Random Forest model by following these steps:
- I used "RandomizedSearchCV" to find the optimal hyperparameters for "n_estimators" (the number of trees) and "max_depth" of the forest.
- I fitted the random search to the training data to identify the best combination of these parameters.
- I created a new `RandomForestRegressor` using the optimal hyperparameters obtained from the search.
- Finally, I trained the model on the entire training dataset and used its predictions to calculate the "Mean Squared Error" (MSE) on the test set.

The Random Forest model had a lower MSE,  so I selected it as the best model.

The project provided valuable insights to help the company become more efficient in inventory planning.

## Analyzing Unicorn Companies
The goal of this project was to identify the top three industries with the highest number of unicorn companies between 2019 and 2021, and to calculate the average valuation for those industries during the same period. (Note: A unicorn company is a private startup with a valuation exceeding $1 billion.)

I completed the project using SQL, sourcing data from four tables that contained information on dates, funding, industries, and companies.

First, I developed a Common Table Expression (CTE) to identify the three industries that had the most new unicorn companies from 2019 to 2021 by doing the following:
- I joined the industries table with the dates table using the company_id.
- I filtered the records to include only those where the year of the date_joined is 2019, 2020, or 2021.
- I then grouped the results by industry and counted the number of companies in each industry.
Finally, I ordered the results in descending order by count and selected only the top three industries using the LIMIT 3 clause.

Next, I developed another CTE to calculate the number of unicorns and their average valuation for all industries between 2019 and 2021 by doing the following:
- I joined the industries, dates, and funding tables together on company_id.
- I grouped the data by industry and the year a company joined.
- I counted the number of companies and calculated the average valuation for each industry per year.

Finally, I wrote a SELECT statement to select from the two CTEs to produce the desired result.

I grouped the data to aggregate the results correctly and ordered the output by year in descending order, and then by the number of unicorns in descending order.

This project provided valuable information to an investment firm, offering insights into industry trends and helping them strategically structure their portfolio for the future.


