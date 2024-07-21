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

# Insights

A single page report was created on Power BI Desktop

Following inferences can be drawn from the dashboard;

### [1] Total Number of Customers = 129880

   Number of satisfied Customers (Male) = 28159 (21.68 %)

   Number of satisfied Customers (Female) = 28269 (21.76 %)

   Number of neutral/unsatisfied customers (Male) = 35822 (27.58 %)

   Number of neutral/unsatisfied customers (Female) = 37630 (28.97 %)


           thus, higher number of customers are neutral/unsatisfied.
           
### [2] Average Ratings

    a) Baggage Handling - 3.63/5
    b) Check-in Service - 3.31/5
    c) Cleanliness - 3.29/5
    d) Ease of online booking - 2.88/5
    e) Food & Drink - 3.21/5
    f) In-flight Entertainment - 3.36/5
    g) In-flight service - 3.64/5
    h) In-flight Wifi service - 2.81/5
    i) Leg room service - 3.37/5
    j) On-board service - 3.38/5
    k) Online boarding - 3.33/5
    l) Seat comfort - 3.44/5
    m) Departure & arrival convenience - 3.22/5
  
  while calculating average rating, null values have been ignored as they were not relevant for some customers. 
  
  These ratings will change if different visual filters will be applied.  
  
  ### [3] Average Delay 
  
      a) Average delay in arrival(minutes) - 15.09
      b) Average delay in departure(minutes) - 14.71
Average delay will change if different visual filters will be applied.

 ### [4] Some other insights
 
 ### Class
 
 1.1) 47.87 % customers travelled by Business class.
 
 1.2) 44.89 % customers travelled by Economy class.
 
 1.3) 7.25 % customers travelled by Economy plus class.
 
         thus, maximum customers travelled by Business class.
 
 ### Age Group
 
 2.1)  21.69 % customers belong to '0-25' age group.
 
 2.2)  52.44 % customers belong to '25-50' age group.
 
 2.3)  25.57 % customers belong to '50-75' age group.
 
 2.4)  0.31 % customers belong to '75-100' age group.
 
         thus, maximum customers belong to '25-50' age group.
         
### Customer Type

3.1) 18.31 % customers have customer type 'First time'.

3.2) 81.69 % customers have customer type 'returning'.
       
       thus, more customers have customer type 'returning'.

### Type of travel

4.1) 69.06 % customers have travel type 'Business'.

4.2) 30.94 % customers have travel type 'Personal'.

        thus, more customers have travel type 'Business'.
