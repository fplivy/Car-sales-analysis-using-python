# Car-sales-analysis-using-python
## INTRODUCTION
The project's goal is to analyse the automobile Sales Dataset, which includes information on various automobile models, manufacturers, and other features in relation to pricing and sales. It is our responsibility to examine the data and respond to the following questions:

- Which manufacturer's average sales volume is higher and which is lower?
- What is the distribution of car prices?
- Do the numerical variables in the dataset show any correlation?
- Which auto brands are the most well-liked?
- Which three vehicles, with engines larger than 2.5 litres, are the most fuel-efficient?

The main goal of this investigation is to demonstrate if car production, cost, and efficiency have increased significantly over time. Python would be used for the study in order to produce charts and carry out statistical analysis in a way that is simple to comprehend.

## DATA SOURCING 
As part of the fourth assessment for the PSP Data Analytics course, which is taught by Mr. Joseph Elijah, the data was obtained from a Google Drive link and published to a WhatsApp group. The assessment question file and the car sales csv file were both inside the folder. 

## PREPARING DATA 
We'll import the required Python libraries to set up the Python environment before we begin analysis. When working with numbers or integers, Pandas, working on series or dataframes, and manipulating data, Numpy is imported. Matplotlib and Seaborn are used for data visualisation. The data was then read in using the CSV format, as seen in the figure below.
 ![image](https://github.com/user-attachments/assets/5ded4877-fe4d-4c20-ab97-0993cf602135)

## DATA EXPLORATION 
Let’s now do an exploration of our data.
- First, we check for the number of rows and columns in the data. There are 157 rows and 16 columns in the dataset
- Next, we check for the datatypes of each column in the car sales data using the “dtypes” function.
 ![image](https://github.com/user-attachments/assets/68cd909c-cfe7-4567-bc27-9d8f056da9a7)

We can see that all columns with string values are classified as “objects” and columns with numbers or decimals are “float” data types, except for the “Launch_date” column classified as objects instead of datetime objects.
 ![image](https://github.com/user-attachments/assets/b79e4195-7a63-4521-a107-cea965c4bc9e)

- We check for missing values in the dataset using “.isna()” function. We count them per columns using the SUM function.

## DATA CLEANSING
Additionally, we thoroughly clean the data before beginning the analysis.

### HANDLING MISSING VALUES
We now address the missing values in the following methods after making sure there are none. 

The year resale value columns include about thirty-six null or missing entries. In order to deal with them, we first calculate the average of all the columns and then substitute those values for the null values. 

The other rows that have missing values are then dropped.
 
### CHANGING COLUMN NAMES
 ![image](https://github.com/user-attachments/assets/a39fca76-7d5c-43d7-b84d-8b9fb3463b6e)

We now remove the leading underscore image from the name of the __year_resale_value column. 

We search the dataset for duplicates, but none are found.

## DESCRIPTIVE STATISTICS 
Using the numerical columns, we will perform a descriptive statistical analysis to determine the mode, mean, median, and other values. Because we only require the number columns, we utilize the describe () function with the whole parameter set. picture 
 ![image](https://github.com/user-attachments/assets/c48e1099-28ba-4cfe-a92b-79a00ee2dbcd)

## Exploratory Data Analysis
1.	 In terms of average sales volume, which manufacturer has the highest and lowest? 
By combining the Manufacturers according to their mean Sales in thousands and then arranging them in either ascending or descending order, we may determine which is highest and lowest. idmax() and idxmin() can also be used in place of sorting to determine the highest and lowest average sales volume, respectively. 
2.	Distribution of car prices in the dataset

 ![image](https://github.com/user-attachments/assets/9bf78df2-bdc8-40d9-8b48-36fedd840001)

Here, we group and plot the Manufacturer with the sum of the Price in thousand.
3.	Correlation matrix of numerical variables in the dataset
 
 ![image](https://github.com/user-attachments/assets/6945e941-9d10-4c04-9d38-f359c17256cf)

4.	Which is the most popular car brands?

 ![image](https://github.com/user-attachments/assets/3a54b2d4-7209-4430-a2d2-d16d7b262846)

By grouping the Manufacturer together with the maximum sales in thousand, we can see that Ford, particularly the F-Series model is the most popular car.
5.	What is the top 3 fuel-efficient cars with an engine size above 2.5 litre

 ![image](https://github.com/user-attachments/assets/bd982f5d-b917-4011-899d-4ff1e90a26f3)

From the image above, the Chevrolet Impala, Chevrolet Monte Carlo and Mercedes CLK Coupe model are the 3 top fuel efficiency cars with an engine size above 2.5 litres.

## CONCLUSION/RECOMMENDATION
Based on our analysis, we’ve been able to provide valuable and data driven answers to our business questions. Recommendation is that a perfect analysis can be done on a wide/large dataset. Visualizations can then be done on PowerBI and other advanced analytics tools.
