# Supermarket_Sales_Analysis

## Exploratory Data Analysis with Python

This project performs an exploratory data analysis (EDA) on a supermarket sales dataset, focusing on customer behavior, sales trends, and performance across branches and product lines.
### Dataset Overview

The dataset contains sales records from a supermarket, including the following columns:

Invoice ID: Unique transaction identifier
- Branch: Store branch (A, B, or C)
- City: Location of the branch
- Customer type: Member or Normal
- Gender: Customer gender
- Product line: Category of the item sold
- Unit price: Price per unit of product
- Quantity: Number of units purchased
- Tax 5%: Tax applied to the purchase
- Total: Total amount (including tax)
- Date: Date of purchase

### Objectives
- Identify sales trends by date and product line.
- Compare performance across branches.
- Analyze customer purchasing behavior by gender and type.
- Evaluate product line profitability and popularity.
- Discover insights from payment methods and gross income.
- Visualize key metrics using plots.

### Tools
- Python
- Pandas & NumPy for data manipulation
- Matplotlib & Seaborn for visualization

### Sample Insights
- Most profitable branch and best-selling product line
- Peak sales days
- Preferred payment method by customer type
- Correlation between rating and gross income

### Sample codes

  #### To determine best selling product lines.
  
       df['Product line'].value_counts()

  ### Plotting a bar plot showing;

  #### Total sales by Gender.

     sns.barplot(x='Gender', y='Total', data=df)

  #### Total sales by customer type

     sns.barplot(x='Customer type', y='Total', data=df)
  ### Time Series trend
  #### Line graph 

     daily_sales = df.groupby('Date')['Total'].sum()
     daily_sales.plot(title="Daily Sales Trend")
### Screenshots

<img width="896" alt="correlation" src="https://github.com/user-attachments/assets/b0825201-8909-4141-99af-3789477c1117" />

   ##### Insights gathered from the correlation.

     Tax 5%, Total, cogs, and gross income are all perfectly positively correlated (1.00),this makes sense since they're mathematically linked.

     Unit price shows a moderate positive correlation (~0.60) with revenue and income,higher priced items = more profit.

     Quantity is not strongly correlated with total sales or income,Could mean higher quantity doesn’t always mean higher revenue (depends on price).

     Rating has almost no correlation with any financial metrics

  #### Gross Income VS Rating
   ##### Screenshot
   <img width="902" alt="correlation 2" src="https://github.com/user-attachments/assets/85921a78-f65d-4a1a-aa27-a9716e32e23e" />

  

                                                                    


     


  
