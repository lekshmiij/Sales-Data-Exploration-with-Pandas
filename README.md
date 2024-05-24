# Sales-Data-Exploration-with-Pandas
This repository contains a project that focuses on exploring a Sales dataset using Pandas. It includes data cleaning, visualization, and statistical analysis to uncover insights and patterns within the data.
![image](https://github.com/lekshmiij/Sales-Data-Exploration-with-Pandas/assets/141242851/f565c917-1fa0-405a-9e97-4bbf8175ddeb)

This project involves the exploration of a sales dataset using Pandas to uncover various insights. Here's a comprehensive overview of the process:

### Merging Monthly Sales Data:

* Sales data from 12 months is merged into a single DataFrame.
* This is done by iterating through the files in the directory, reading each CSV file, and concatenating them into one DataFrame.
* The merged data is saved as all_data.csv.
  
### Loading and Initial Exploration:
* The combined dataset is loaded using pd.read_csv.
* Basic exploration is done with .head() to inspect the first few rows of the dataset.

### Data Preprocessing:
* Missing values are identified using .isnull().sum().
* Rows with all missing values are dropped using dropna(how='all').
* A new column Month is extracted from the Order Date column.
* Non-date rows (e.g., containing "Or") are filtered out.
* The Month column is converted to integers.

### Calculating Monthly Sales:
* Columns Quantity Ordered and Price Each are converted to numeric types.
* A new Sales column is created by multiplying Quantity Ordered by Price Each.
* Sales data is grouped by month and summed to find the month with the highest sales.
* A bar plot is created to visualize monthly sales.

### City with Most Sales:

* City and state are extracted from the Purchase Address column.
* A new City column is created combining city and state.
* Sales data is grouped by city and summed to find the city with the highest sales.

### Optimal Advertisement Timing:
* The Order Date column is converted to datetime format.
* New columns Hour and Minute are created from the Order Date.
* Sales data is grouped by hour to find the best time for advertisements.
* A line plot is created to visualize sales by hour.
  
### Identifying Products Sold Together:
* Orders with duplicated Order ID are identified.
* Products in the same order are grouped together.
* Combinations of products sold together are counted using Counter from the collections module.
* The most common product pairs are identified.

### Most Sold Product and Reasons:
* Sales data is grouped by product.
* The total quantity ordered for each product is calculated.
* Insights are drawn on the most sold product and potential reasons.
  
This comprehensive process involves data merging, cleaning, feature engineering, analysis, and visualization to gain insights into sales patterns, optimal advertisement timings, and product pairings.


#### _Dataset Description_
- Order ID: A unique identifier for each order.
- Product: The name of the product ordered.
- Quantity Ordered: The quantity of the product ordered in each transaction.
- Price Each: The price of one unit of the product.
- Order Date: The date and time when the order was placed.
- Purchase Address: The address where the purchase was made, including the city, state, and ZIP code.
