# Analyzing sales data using Python
Analyzing sales data in Jupyter Notebook using Python, pandas and matplotlib.

## Scenario

**Data set**

The data set includes 12 months' worth of sales data, which contains hundreds of thousands of electronics store orders broken down by product type, quantity ordered, price, order date, and purchase address.

## Task

**Answering questions**

- What was the best month for sales? How much was earned that month?

- What city sold the most products?

- What time should ads be displayed to maximize the likelihood of customers buying products?

- What combination of products are most often sold together?

- What product sold the most and why?

## What I Did

**Python libraries used**

- Pandas
- Matplotlib.pyplot
- Matplotlib.ticker
- Counter
- Combinations

### Tasks completed to answer each business question

**Data cleaning**

- Drop NaN values from the DataFrame

- Remove rows based on a condition

- Change the type of columns depending on the column (to_numeric, to_datetime, astype)

**Specific tasks**

- What was the best month for sales? How much was earned that month?
    - Add a month and sales column
    - Plot bar chart with Month as the x-axis and Sales ($) as the y-axis
    - Format matplotlib plot style as needed

- What city sold the most products?
    - Add a city and state column
    - Group the dataframe by city and apply the sum function to get the total Sales for each city
    - Plot bar chart with city as the x-axis and Sales ($) as the y-axis
    - Format matplotlib plot style to change the orientation of x-axis labels to vertical

- What time should ads be displayed to maximize the likelihood of customers buying products?
     - Convert Order Date column to datetime
     - Create Hour and Minute columns
     - Count the occurrences of orders, grouped by the hour
     - Plot line chart to determine what time of day has the highest number of orders
     - Format line chart to add x-axis grid to make it easier to follow the trend

- What combination of products are most often sold together?
     - Import itertools and collections libraries
     - Count how often 2 items were bought together by combining products with the same Order ID into pairs
     - Get the top 10 combinations of items most often bought together

- What product sold the most and why?
     - Sum on Product (count) and plot bar chart for each product
     - Determine correlation between price and quantity ordered to answer "why"
     - Plot Price as a secondary y-axis to visualize correlation
     - Format charts to configure colors and label padding
