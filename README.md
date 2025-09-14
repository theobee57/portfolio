# My Data Science Portfolio

## Projects
## New Product Sales Strategy
![Sales Strategies](/images/Sales_strategies.png)       
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
### Objective
The objective of this project was to conduct exploratory data analysis on Netflix data to uncover insights into movies from the 1990s, a pivotal decade in the modern film industry, and provide answers to specific business questions.
i
### Tools
I  used Pandas for manipulating the dataset, Matplotlib for visualization, and Python for programming.
### Procedure
Having loaded pre-cleaned Netflix data into a pandas DataFrame, I subsetted the DataFrame to include only movies released between 1990 and 1999.

I then created a histogram based on the 'Duration' column. This visualization enabled me to determine the distribution of movie lengths in that decade, especially the most common movie duration and other insights.

I applied a second filter to isolate the 'Action' genre. Then I iterated through this filtered dataset using a for loop with a counter variable to count each movie that met various duration criteria.
### Impact
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

## Hypothesis Testing With Men's and Women's Soccer Matches

##  Clustering Antarctic Penguin Species

## Predicting Movie Rental Durations 


