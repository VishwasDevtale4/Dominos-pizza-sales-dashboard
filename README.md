# PizzaSales-Dashboard

## Problem Statement

This dashboard helps Domino's pizza outlet in Mumbai, using Power BI report to uncover actionable insights to help the outlet increase sales and improve operational efficiency. This report identifies trends in pizza orders, customer preferences, and sales performance, and recommend strategies to optimize the menu, pricing, and promotional activities.

1) Analyze total sales over time to identify peak periods.
2) Assess sales by pizza type and size to understand popular choices.
3) List of best value for price: Price vs Quantity
4) Examine the frequency and quantity of orders by time of day and week to understand customer habits.
5) Identify any correlations between pizza types and specific times or dates.
6) Evaluate the performance of individual pizza types
7) Evaluate the performance at different categories (Veg-Non veg, Pizza Mania, pasta,Taco)
8) Weekday vs Weekend trend
9) Most bought combinations
10) Seasonality in pizzas

### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & merged four tables to take actionable insights out of them.
- Step 3 : Checked for null values in all the columns.
- Step 4 : Created a custom column to distinguis between veg ans non-veg pizzas.
- Step 5 : Created a custom column "Weekdays" to extract the day name based on the order date.
- Step 6 : Created a custom column "Price-Range" to assign each pizza to a specific price bracket.
- Step 7 : Created a new table "Measures" to store all the DAX functions under it. 
- Step 8 : Card visuals were added to display multiple metrics such as "Total Revenue", "Total Pizza Sold", "Total Number of Orders", "Average Order Value", and "Average Pizza per Order".
           
           Although, by default, while calculating average, blank values are ignored.

- Step 9 : A bar chart was also added to the report design area representing Quantity Sold by category, weekly sales and least selling products.
- Step 10 : Created a slicer for the "category" field to enable analysis of sales categorized by different categories. 
- Step 11 : Multi-row visual was added to the canvas to display two important filed "Top 5 produscts by revenue" and "Bottom 5 produscts by revenue".
- Step 12 : Funnel visualiztion was added to display price range v/s sales report.
- Step 13 :  A doughnut chart visual was added to display the top 5 best-selling pizzas, and a pie chart visual was added to show the distribution of sales by pizza size.
- Step 14 : In the report view, under the insert tab, using shapes option from elements group a rectangle was inserted & similarly using image option company's logo was added to the report design area. 


for creating new column following DAX expression was written;
       
       Average order value = DIVIDE([Total Revenue],[Total No. Of Orders])
        
- Step 15 : New measure was created to find total revenue.

Following DAX expression was written for the same,
        
        Total Revenue = SUM(order_details[pizzas.Price])
    
A card visual was used to represent Total Revenue.

![image](https://github.com/user-attachments/assets/e4ebbfc7-7e91-4663-bb91-891ede1d4e8c)

        
 - Step 16 : New measure was created to find total pizza sold
 
 Following DAX expression was written to find total pizza sold
 
         Total Pizza Sold = SUM(order_details[quantity])
 
 A card visual was used to represent this number.
 
 Snap of matrix to show total pizza sold.
 
 ![image](https://github.com/user-attachments/assets/01909911-3483-4914-ad2b-8b947638607c)

 
 - Step 17 : New measure was created to find average pizza per order.
 
 Following DAX expression was written to find average pizza per order
 
         Avg Pizza Per Order = DIVIDE([Total Pizza Sold],[Total No. Of Orders])
 
 A card visual was used to represent this number.
 
 Snap of matrix to show average pizza per order sold.

 ![image](https://github.com/user-attachments/assets/3f27b46b-c882-4734-97e8-73e160ad1808)
 

 # Report Snapshot (Power BI DESKTOP)

 ![image](https://github.com/user-attachments/assets/712ef5e5-dfe3-4315-9b81-bada188c295f)

## Key Insights

### Best-Performing Pizzas
- **Top 5 Bestselling Pizzas:**
  1. **Fresh Veggie:** 23.16%
  2. **Double Cheese Margherita:** 21.9%
  3. **Cheese n Corn:** 19.46%
  4. **Deluxe Veggie:** 17.86%
  5. **Chicken Golden Delight:** 17.86%

### Revenue Insights
- **Top 5 Products by Revenue:**
  1. **Chicken Golden Delight:** 1,563,919
  2. **Fresh Veggie:** 1,460,037
  3. **Deluxe Veggie:** 1,207,564
  4. **Double Cheese Margherita:** 1,250,508
  5. **Indi Tandoori Paneer:** 1,212,383

### Sales Insights
- **Quantity Sold by Category:**
  - **Veg Pizza:** 27K
  - **Non-Veg Pizza:** 15K
  - **Taco:** 4K
  - **Cake:** 1K
  - **Others:** 0K (Not contributing significantly)

### Least Selling Products
- **Red Velvet:** 289
- **Crinkle Fries:** 276
- **Veg Loaded:** 276
- **Non-Veg Loaded:** 99
- **Garlic Breadsticks:** 28

### Sales Trends
- **Monthly Sales:**
  - Peak in July with 4,299 sales.
  - Steady sales around 4,000 units per month.
- **Weekly Sales:**
  - Highest sales on Sunday with 8.1K.
  - Steady sales through the week with a drop on Tuesday (5.9K).

### Price Range Insights
- Majority of sales (38.7%) in the price range 200-400.
- Sales gradually decrease as the price range increases.

### Pizza Size Insights
- **Large (L):** 34.8%
- **Regular (R):** 34.7%
- **Medium (M):** 30.4%

### Conclusion
- **Top-Performing Pizza:** Fresh Veggie, both in terms of quantity sold and revenue generated.
- **Popular Pizza Sizes:** Large and Regular sizes are almost equally popular.
- **Sales Trends:** Higher sales towards the end of the week, especially on Fridays.
- **Revenue Generation:** Chicken Golden Delight leads in revenue, indicating a high price point or high sales volume.

