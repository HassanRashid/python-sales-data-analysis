## Analyzing sales data using Python pandas and matplotlib
Analyzing sales data in Jupyter Notebook using Python, pandas and matplotlib.

Output: https://github.com/HassanRashid/python-sales-data-analysis/blob/main/Sales_Analysis.ipynb

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

- Itertools (Combinations)

- Collections (Counter)

### Tasks completed to answer each business question

**Setup**

- Merge .CSV files together (187,000 rows of data)

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

## Results

- What was the best month for sales? How much was earned that month?
    - December, $46m

- What city sold the most products?
    - San Fransisco, CA, $80m

- What time should ads be displayed to maximize the likelihood of customers buying products?
    - Around 12pm and 7pm (decision lag not taken into account)

- What combination of products are most often sold together?
    - iPhone and Lightning Charging Cable (1005 times)
    - Google Phone and USB-C Charging Cable (987 times)
    - iPhone and Wired Headphones (447 times)

- What product sold the most and why?
    - AAA/AA Batteries
    - USB-C Charging Cable
    - Lightning Charging Cable
    - Correlation between price and quantity ordered shows that products with a lower price (AAA batteries, for example) sold more quantities as opposed to products with higher prices (LG washing machine, for example)
