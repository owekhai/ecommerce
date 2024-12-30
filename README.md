# E-commerce Analysis

## Table of Contents

- [Data Description](#dataset-description)
- [Content](#content)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Cleaning](#data-cleaning)
- [Inference Analysis](#inference-analysis)
- [Findings](#findings)
- [Recommendations](#recommendations)
- [Limitations](#limitations)
- [Conclusion](#conclusion)

### Dataset Description
An international e-commerce company specializing in electronic products is on a quest to extract pivotal insights from their customer database. Their approach involves the application of advanced machine learning techniques to scrutinize and understand their diverse customer base, in efforts to enhance their operations and sales strategies.

### Content 
 The dataset comprises 10,999 observations across 12 variables, each illuminating different facets of the company's operations and customer interactions:

- ID: Customer identification number.
- Warehouse block: The company's extensive warehouse is segmented into blocks (A, B, C, D, E) for efficient product management.
- Mode of shipment: Products are shipped through various means, including Ship, Flight, and Road.
- Customer care calls: The number of calls initiated for shipment inquiries.
- Customer rating: The company has assessed every customer with ratings from 1 (lowest, worst) to 5 (highest, best).
- Cost of the product: Product cost in US Dollars.
- Prior purchases: The number of previous purchases made by the customer.
- Product importance: Products are categorized into low, medium, or high importance based on specific parameters.
- Gender: Customer gender, categorized as Male and Female.
- Discount offered: The discount offered on specific products.
- Weight in grams: The weight of the product in grams.
- Reached on time: The target variable; 1 indicates that the product did not reach on time, while 0 indicates on-time delivery.
- Goal: To assertain the reason why customers are having low ratings and why customers are opting for ship as the mode of shipment as against others.

### Data Sources

The data source is a CSV file named "ecommerce.csv" which is gotten from techrative technology limited as a capstone project

### Tools:
 * Python programming language
 * pandas for data manipulation and analysis
 * NumPy for numerical operations
 * matplotlib and seaborn for data visualization
 * plotly for interactive visualizations
 * sqlite3 for SQL queries (although the data is initially loaded from a CSV)

### Data Cleaning
* 1. Removal of the 'ID' column: deemed unnecessary for analysis.
* 2. Duplicate value check: no duplicates found.
* 3. Null/empty value check: no missing data detected.
 
### Inference Analysis
  The analysis uses several techniques:
* 1. Correlation Matrix (heatmap):  Examines relationships between variables.
* 2. Value Counts & Bar Charts: Analyzes the frequency of shipment modes, product importance, and customer ratings.
* 3. Grouped Bar Charts: Shows the relationship between shipment mode and on-time delivery.
* 4. Box Plots: Compares the weight of products shipped by different modes.
* 5. Count Plots: Visualizes product importance and on-time delivery.
* 6. Pie Charts: Displays the distribution of customer ratings.
* 7. Sunburst Plots: Explores relationships among gender, shipment mode, product importance, warehouse block, and cost.
* 8. Contingency Tables: Shows the relationship between mode of shipment and customer rating.
* 9. SQL Queries:  Additional analysis via SQL queries on an SQLite database created from the DataFrame (e.g., filtering for high cost, product importance, discounts).
 
### Findings
* "Ship" is the most frequent shipment mode.
* There's a negative correlation between several variables (further investigation required to understand the nature of these relationships).
* Ship mode has a high percentage of on-time deliveries compared to other methods.
* Product importance seems to affect on-time delivery. High importance products seem to be delivered on time more frequently, but the countplot doesn't conclusively demonstrate this.
* Customer ratings are centered around 3.
* The cost of products appears to vary with gender, shipment mode, and product importance.

### Recommendations
1. **Focus on "Ship" improvements**: Since "Ship" is the dominant mode and the results don't indicate a huge difference in the on-time delivery among the various shipping modes, optimize the "Ship" process for even better on-time delivery.  This could be done by investigating shipping routes, partnerships, or warehouse management.

2. **Investigate low customer ratings:** Further analysis is needed to understand why customer ratings center around "3."  Explore customer feedback to identify areas for improvement. A deeper dive into the characteristics of customers giving low ratings might provide valuable insights.

3. **Product Importance Segmentation**:  Analyze the factors influencing "high importance" product classifications more closely.  If this category corresponds to premium products, they may be experiencing a different set of challenges that warrant further investigation.

4. **Discount Optimization**: Understand the relationship between discounts and customer ratings.  Test the impact of different discount strategies, potentially optimizing for higher ratings rather than just sales.


### Limitations
1. **Lack of detailed customer feedback data**: Customer feedback would significantly enhance understanding of the rating distributions and offer targeted ways to improve customer satisfaction.

2. **Missing context on "high importance" products**: More information is needed to identify any special handling or processes associated with high-importance products.

### Conclusion
- The enitre distribution shows that low product do arrive on time as against other product
- The shipment of product is mostly convey with ship with high rating
- Customer prefer using ship to convey product that has great mass of weight because of the discount.
- High discount shows high product rating, for other product to receive high product ratings from customers they need to step up the ratings for other products.


