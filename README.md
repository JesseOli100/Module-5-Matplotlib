# Module-5-Matplotlib

# Background

You've just joined Pymaceuticals, Inc., a new pharmaceutical company that specializes in anti-cancer medications. Recently, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer.

As a senior data analyst at the company, you've been given access to the complete data from their most recent animal study. In this study, 249 mice who were identified with SCC tumors received treatment with a range of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals’ drug of interest, Capomulin, against the other treatment regimens.

The executive team has tasked you with generating all of the tables and figures needed for the technical report of the clinical study. They have also asked you for a top-level summary of the study results.

# Instructions

This assignment is broken down into the following tasks:

Prepare the data.

Generate summary statistics.

Create bar charts and pie charts.

Calculate quartiles, find outliers, and create a box plot.

Create a line plot and a scatter plot.

Calculate correlation and regression.

Submit your final analysis.

# Prepare the Data

Run the provided package dependency and data imports, and then merge the mouse_metadata and study_results DataFrames into a single DataFrame.

Display the number of unique mice IDs in the data, and then check for any mouse ID with duplicate time points. Display the data associated with that mouse ID, and then create a new DataFrame where this data is removed. Use this cleaned DataFrame for the remaining steps.

Display the updated number of unique mice IDs.

# Generate Summary Statistics

Create a DataFrame of summary statistics. Remember, there is more than one method to produce the results you're after, so the method you use is less important than the result.

Your summary statistics should include:

A row for each drug regimen. These regimen names should be contained in the index column.

A column for each of the following statistics: mean, median, variance, standard deviation, and SEM of the tumor volume.

# Create Bar Charts and Pie Charts

Generate two bar charts. Both charts should be identical and show the total total number of rows (Mouse ID/Timepoints) for each drug regimen throughout the study.

Create the first bar chart with the Pandas DataFrame.plot() method.

Create the second bar chart with Matplotlib's pyplot methods.

Generate two pie charts. Both charts should be identical and show the distribution of female versus male mice in the study.

Create the first pie chart with the Pandas DataFrame.plot() method.

Create the second pie chart with Matplotlib's pyplot methods.

# Calculate Quartiles, Find Outliers, and Create a Box Plot

Calculate the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. Then, calculate the quartiles and IQR, and determine if there are any potential outliers across all four treatment regimens. Use the following substeps:

Create a grouped DataFrame that shows the last (greatest) time point for each mouse. Merge this grouped DataFrame with the original cleaned DataFrame.

Create a list that holds the treatment names as well as a second, empty list to hold the tumor volume data.

Loop through each drug in the treatment list, locating the rows in the merged DataFrame that correspond to each treatment. Append the resulting final tumor volumes for each drug to the empty list.

Determine outliers by using the upper and lower bounds, and then print the results.

Using Matplotlib, generate a box plot that shows the distribution of the final tumor volume for all the mice in each treatment group. Highlight any potential outliers in the plot by changing their color and style.

hint: All four box plots should be within the same figure. Use this Matplotlib documentation pageLinks to an external site. for help with changing the style of the outliers.

# Create a Line Plot and a Scatter Plot

Select a single mouse that was treated with Capomulin, and generate a line plot of tumor volume versus time point for that mouse.

Generate a scatter plot of mouse weight versus average observed tumor volume for the entire Capomulin treatment regimen.

# Calculate Correlation and Regression

Calculate the correlation coefficient and linear regression model between mouse weight and average observed tumor volume for the entire Capomulin treatment regimen.

Plot the linear regression model on top of the previous scatter plot.

# Sources

• Help from TA Matthew Werth and other staff

• Met up w/ other students during study groups to hash out the code through what we have learned so far

• Used StackOverFlow and ChatGPT for issues on the code and/or to explain why certain pieces of the script were not running as intended

# Notes

What is the code supposed to be doing? What is the purpose of this exercise? 

The main purpose of this exercise is to really put to the test the things we have learned in class so far and show that we can create various types of graphs, lines, plots, and charts with different information pulled from the dataset we’ve been given. Overall, this is a fun project as I got to explore all the material learned in recent classes all on my own. 

Syntax Learned:

•	.merge() - is used to merge two or more pandas DataFrames based on a common column or index. It is similar to the SQL JOIN operation.

•	.loc - is used to access a group of rows and columns by labels or a boolean array. It is primarily used with pandas DataFrames and Series for label-based indexing.

•	.var() - is used to calculate the variance of a set of values.

•	.std() - is used to calculate the standard deviation of a set of values. This function is often applied to pandas Series or NumPy arrays. Standard deviation is a measure of the amount of variation or dispersion in a set of values.

•	.sem() - is used to calculate the standard error of the mean (SEM) of a set of values. The standard error of the mean is a measure of how much the sample mean is expected to vary from the true population mean.

•	autopct= - is used with pie charts to display the percentage distribution of each wedge. This is optional, and if not specified, percentages won’t be displayed on the pie chart

•	.isin() – is used to filter data frames or series based on a particular set of values. It is often used to select rows that have values present in a specified list or another iterable.

•	.iloc – is used for integer-location based indexing. It allows for the selection of rows and columns from a dataframe or series by specifying integer indices.

•	.stack() – is a function used to convert the data from a wide format (with multiple columns) to a long format, specifically creating a multi-index series. This operation is often used as “stacking” because it effectively stacks the specified levels of a dataframe’s columns into a single level, resulting in a series with a multi-index.

•	.unstack() – is the reverse operation of the .stack() function when working with dataframes. It is used to pivot a level of the multi-index labels, effectively transforming a multi-level index into multiple columns. This operation is often referred to as “unstacking.” 

•	.quantile() – is used to compute the quantile of a set of data. Quantiles are values that divide the dataset into intervals of equal provability. The most commonly used quantiles are the median (quantile 0.5), quartiles (quantiles 0.25, 0.5, and 0.75), and percentiles (quantiles expressed as a percentage, the 25th, 50th, and 75th percentiles). 

•	.dropna() – this method is used to remove missing (NaN) values from a dataframe or series. It is a convenient way to clean or pre-process data by eliminating rows or columns that contain missing values. 

- - - - - - 

This is submitted by Jesse Olivarez for the University of Utah: Data Analytics Bootcamp
