<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
  
<body style="font-family: 'Arial', sans-serif; line-height: 1.6; margin: 0 auto; max-width: 800px; padding: 20px; background-color: #f9f9f9; color: #333;">
    <h1 style="color: #2c3e50; border-bottom: 2px solid #3498db; padding-bottom: 10px;">DSA Data Analysis Capstone Project</h1>

    
  <h2 style="color: #2980b9; margin-top: 20px;">Introduction</h2>
    <p style="margin: 10px 0;">Hi, I'm <b style="font-weight: bold;">Oluwasegun Salako</b>, a data analyst. This repository showcases my work on the <i style="font-style: italic;">DSA Data Analysis Capstone Project</i>, where I analyzed the <span style="background-color: #ffeaa7; padding: 2px 5px; border-radius: 3px;">Kultra Mega Stores Inventory</span> dataset to answer key business questions using SQL. The project demonstrates my ability to perform comprehensive exploratory data analysis (EDA) and derive actionable insights from large datasets.</p>

  <h2 style="color: #2980b9; margin-top: 20px;">Project Overview</h2>
    <p style="margin: 10px 0;">The goal of this project was to analyze order data from Kultra Mega Stores (KMS) to provide insights into sales performance, customer behavior, and shipping efficiency. By addressing specific questions from the case study, I aimed to help KMS optimize its operations and improve profitability. The analysis was conducted using SQL queries on a dataset containing order details from 2009 to 2012.</p>

  <h3 style="color: #34495e; margin-top: 15px;">Dataset Description</h3>
    <p style="margin: 10px 0;">The dataset, stored in the <code style="background-color: #ecf0f1; padding: 2px 5px; border-radius: 3px;">KMS SQL Case Study</code>, renamed as <code style="background-color: #ecf0f1; padding: 2px 5px; border-radius: 3px;">job-tracker-462912.Capstone.capstone_corrected</code> table, consists of 8,400 rows and 21 columns, including:</p>
    <ul style="list-style-type: square; margin-left: 20px;">
        <li style="margin: 5px 0;"><code style="background-color: #ecf0f1; padding: 2px 5px; border-radius: 3px;">Row_ID</code></li>
        <li style="margin: 5px 0;"><code style="background-color: #ecf0f1; padding: 2px 5px; border-radius: 3px;">Order_ID</code></li>
        <li style="margin: 5px 0;"><code style="background-color: #ecf0f1; padding: 2px 5px; border-radius: 3px;">Order_Date</code></li>
        <li style="margin: 5px 0;"><code style="background-color: #ecf0f1; padding: 2px 5px; border-radius: 3px;">Order_Priority</code></li>
        <li style="margin: 5px 0;"><code style="background-color: #ecf0f1; padding: 2px 5px; border-radius: 3px;">Order_Quantity</code></li>
        <li style="margin: 5px 0;"><code style="background-color: #ecf0f1; padding: 2px 5px; border-radius: 3px;">Sales</code></li>
        <li style="margin: 5px 0;"><code style="background-color: #ecf0f1; padding: 2px 5px; border-radius: 3px;">Discount</code></li>
        <li style="margin: 5px 0;"><code style="background-color: #ecf0f1; padding: 2px 5px; border-radius: 3px;">Ship_Mode</code></li>
        <li style="margin: 5px 0;"><code style="background-color: #ecf0f1; padding: 2px 5px; border-radius: 3px;">Profit</code></li>
        <li style="margin: 5px 0;"><code style="background-color: #ecf0f1; padding: 2px 5px; border-radius: 3px;">Unit_Price</code></li>
        <li style="margin: 5px 0;"><code style="background-color: #ecf0f1; padding: 2px 5px; border-radius: 3px;">Shipping_Cost</code></li>
        <li style="margin: 5px 0;"><code style="background-color: #ecf0f1; padding: 2px 5px; border-radius: 3px;">Customer_Name</code></li>
        <li style="margin: 5px 0;"><code style="background-color: #ecf0f1; padding: 2px 5px; border-radius: 3px;">Province</code></li>
        <li style="margin: 5px 0;"><code style="background-color: #ecf0f1; padding: 2px 5px; border-radius: 3px;">Region</code></li>
        <li style="margin: 5px 0;"><code style="background-color: #ecf0f1; padding: 2px 5px; border-radius: 3px;">Customer_Segment</code></li>
        <li style="margin: 5px 0;"><code style="background-color: #ecf0f1; padding: 2px 5px; border-radius: 3px;">Product_Category</code></li>
        <li style="margin: 5px 0;"><code style="background-color: #ecf0f1; padding: 2px 5px; border-radius: 3px;">Product_Sub_Category</code></li>
        <li style="margin: 5px 0;"><code style="background-color: #ecf0f1; padding: 2px 5px; border-radius: 3px;">Product_Name</code></li>
        <li style="margin: 5px 0;"><code style="background-color: #ecf0f1; padding: 2px 5px; border-radius: 3px;">Product_Container</code></li>
        <li style="margin: 5px 0;"><code style="background-color: #ecf0f1; padding: 2px 5px; border-radius: 3px;">Product_Base_Margin</code></li>
        <li style="margin: 5px 0;"><code style="background-color: #ecf0f1; padding: 2px 5px; border-radius: 3px;">Ship_Date</code></li>
    </ul>


  ![DATASHEET](https://github.com/user-attachments/assets/3bbaaf27-22d5-4bb9-92f6-73e163fe5cf1)

    
  <p style="margin: 10px 0;">This dataset provides a comprehensive view of KMS's sales, customer segments, and shipping methods over a four-year period.</p>

   <h3 style="color: #34495e; margin-top: 15px;">Key Findings</h3>
    <ul style="list-style-type: square; margin-left: 20px;">
        <li style="margin: 5px 0;"><b style="font-weight: bold;">Sales Performance</b>: The <span style="background-color: #ffeaa7; padding: 2px 5px; border-radius: 3px;">Technology</span> category had the highest sales, driven by high-value items like copiers and telephones.</li>
        <li style="margin: 5px 0;"><b style="font-weight: bold;">Regional Analysis</b>: Alberta (West) was the top-performing region, while Nunavut had the lowest sales.</li>
        <li style="margin: 5px 0;"><b style="font-weight: bold;">Customer Insights</b>: The most valuable customers, such as Raymond Book and Christine Abelman, primarily purchased from the <span style="background-color: #ffeaa7; padding: 2px 5px; border-radius: 3px;">Technology</span> and <span style="background-color: #ffeaa7; padding: 2px 5px; border-radius: 3px;">Furniture</span> categories.</li>
        <li style="margin: 5px 0;"><b style="font-weight: bold;">Shipping Efficiency</b>: KMS incurred the highest shipping costs using the <span style="background-color: #ffeaa7; padding: 2px 5px; border-radius: 3px;">Delivery Truck</span> method, despite it being the most economical option, suggesting potential overuse for non-urgent orders.</li>
    </ul>

   <h2 style="color: #2980b9; margin-top: 20px;">Analysis and SQL Queries</h2>
    <p style="margin: 10px 0;">I used SQL to extract and analyze the data, addressing each question from the case study. The queries involved aggregating sales and profit data, filtering by customer segments and regions, and grouping by product categories and shipping methods. These queries allowed me to identify trends, such as the dominance of the Technology category and the need for better alignment between shipping methods and order priorities.</p>

  <h3 style="color: #34495e; margin-top: 15px;">Question 1: Which product category had the highest sales?</h3>
    <pre style="background-color: #ecf0f1; padding: 10px; border-radius: 5px; overflow-x: auto;"><code>SELECT Product_Category, SUM(Sales) AS Total_Sales
FROM `job-tracker-462912.Capstone.capstone_corrected`
WHERE Sales IS NOT NULL
GROUP BY Product_Category
ORDER BY Total_Sales DESC
LIMIT 1;</code></pre>
    <p style="margin: 10px 0;"><b style="font-weight: bold;">Insight</b>: The <span style="background-color: #ffeaa7; padding: 2px 5px; border-radius: 3px;">Technology</span> category had the highest sales, driven by high-value items like copiers and telephones.</p>


![Question 1](https://github.com/user-attachments/assets/0f7c703d-3d8e-4fe4-8e78-15d24be61f29)


   <h3 style="color: #34495e; margin-top: 15px;">Question 2: What are the Top 3 and Bottom 3 regions in terms of sales?</h3>
    <pre style="background-color: #ecf0f1; padding: 10px; border-radius: 5px; overflow-x: auto;"><code>SELECT Region, SUM(Sales) AS Total_Sales
FROM `job-tracker-462912.Capstone.capstone_corrected`
WHERE Sales IS NOT NULL
GROUP BY Region
ORDER BY Total_Sales DESC;</code></pre>
    <p style="margin: 10px 0;"><b style="font-weight: bold;">Insight</b>: 
        <ul style="list-style-type: square; margin-left: 20px;">
            <li style="margin: 5px 0;"><b style="font-weight: bold;">Top 3</b>: Alberta (West), Northwest Territories, Nunavut.</li>
            <li style="margin: 5px 0;"><b style="font-weight: bold;">Bottom 3</b>: Nunavut, Northwest Territories, Alberta (West).</li>
        </ul>
    </p>


![question 2](https://github.com/user-attachments/assets/761b142b-54ab-41ee-8bb8-a8314050b8cf)



   <h3 style="color: #34495e; margin-top: 15px;">Question 3: What were the total sales of appliances in Ontario?</h3>
    <pre style="background-color: #ecf0f1; padding: 10px; border-radius: 5px; overflow-x: auto;"><code>SELECT SUM(Sales) AS Total_Appliance_Sales
FROM `job-tracker-462912.Capstone.capstone_corrected`
WHERE Product_Sub_Category = 'Appliances' AND Province = 'Ontario'
AND Sales IS NOT NULL;</code></pre>
    <p style="margin: 10px 0;"><b style="font-weight: bold;">Insight</b>: There were no appliance sales in Ontario, as the dataset does not include Ontario records.</p>


![question 3](https://github.com/user-attachments/assets/662db15f-f5c9-4975-a487-79bf8e72ecd5)



  <h3 style="color: #34495e; margin-top: 15px;">Question 4: Advise the management of KMS on what to do to increase the revenue from the bottom 10 customers.</h3>
    <pre style="background-color: #ecf0f1; padding: 10px; border-radius: 5px; overflow-x: auto;"><code>SELECT Customer_Name, SUM(Sales) AS Total_Sales
FROM `job-tracker-462912.Capstone.capstone_corrected`
WHERE Sales IS NOT NULL
GROUP BY Customer_Name
ORDER BY Total_Sales ASC
LIMIT 10;</code></pre>
    <p style="margin: 10px 0;"><b style="font-weight: bold;">Insight</b>: The bottom 10 customers (e.g., Aaron Bergman, Cyma Kinney) have low sales. KMS should implement targeted promotions, cross-selling, and personalized marketing to increase their spending.</p>


![4](https://github.com/user-attachments/assets/aa93f956-a1c7-403b-aca4-384731372a00)



   <h3 style="color: #34495e; margin-top: 15px;">Question 5: KMS incurred the most shipping cost using which shipping method?</h3>
    <pre style="background-color: #ecf0f1; padding: 10px; border-radius: 5px; overflow-x: auto;"><code>SELECT Ship_Mode, SUM(Shipping_Cost) AS Total_Shipping_Cost
FROM `job-tracker-462912.Capstone.capstone_corrected`
WHERE Shipping_Cost IS NOT NULL
GROUP BY Ship_Mode
ORDER BY Total_Shipping_Cost DESC
LIMIT 1;</code></pre>
    <p style="margin: 10px 0;"><b style="font-weight: bold;">Insight</b>: <span style="background-color: #ffeaa7; padding: 2px 5px; border-radius: 3px;">Delivery Truck</span> incurred the highest shipping costs, likely due to its frequent use for heavy or bulky items.</p>


![5](https://github.com/user-attachments/assets/ac9b0bd1-1a34-46d9-a00d-f3a634babc59)



  <h3 style="color: #34495e; margin-top: 15px;">Question 6: Who are the most valuable customers, and what products or services do they typically purchase?</h3>
    <pre style="background-color: #ecf0f1; padding: 10px; border-radius: 5px; overflow-x: auto;"><code>WITH ValuableCustomers AS (
  SELECT Customer_Name, SUM(Sales) AS Total_Sales, SUM(Profit) AS Total_Profit, COUNT(*) AS Order_Count
  FROM `job-tracker-462912.Capstone.capstone_corrected`
  WHERE Sales IS NOT NULL AND Profit IS NOT NULL
  GROUP BY Customer_Name
  ORDER BY Total_Sales DESC, Total_Profit DESC, Order_Count DESC
  LIMIT 5
)
SELECT 
  vc.Customer_Name,
  vc.Total_Sales,
  vc.Total_Profit,
  vc.Order_Count,
  p.Product_Category,
  p.Product_Sub_Category,
  COUNT(*) AS Purchase_Count
FROM ValuableCustomers vc
JOIN `job-tracker-462912.Capstone.capstone_corrected` p
  ON vc.Customer_Name = p.Customer_Name
GROUP BY 
  vc.Customer_Name,
  vc.Total_Sales,
  vc.Total_Profit,
  vc.Order_Count,
  p.Product_Category,
  p.Product_Sub_Category
ORDER BY vc.Total_Sales DESC, Purchase_Count DESC;</code></pre>
    <p style="margin: 10px 0;"><b style="font-weight: bold;">Insight</b>: The most valuable customers (e.g., Raymond Book, Christine Abelman) typically purchase high-value items from <span style="background-color: #ffeaa7; padding: 2px 5px; border-radius: 3px;">Technology</span> and <span style="background-color: #ffeaa7; padding: 2px 5px; border-radius: 3px;">Furniture</span> categories.</p>


![6](https://github.com/user-attachments/assets/078af889-7211-4cc8-b1bd-06ce9138a196)



   <h3 style="color: #34495e; margin-top: 15px;">Question 7: Which small business customer had the highest sales?</h3>
    <pre style="background-color: #ecf0f1; padding: 10px; border-radius: 5px; overflow-x: auto;"><code>SELECT Customer_Name, SUM(Sales) AS Total_Sales
FROM `job-tracker-462912.Capstone.capstone_corrected`
WHERE Customer_Segment = 'Small Business' AND Sales IS NOT NULL
GROUP BY Customer_Name
ORDER BY Total_Sales DESC
LIMIT 1;</code></pre>
    <p style="margin: 10px 0;"><b style="font-weight: bold;">Insight</b>: <span style="background-color: #ffeaa7; padding: 2px 5px; border-radius: 3px;">Carlos Soltero</span> had the highest sales among small business customers, driven by purchases like the Sharp Copier.</p>


![7](https://github.com/user-attachments/assets/bec317a4-bf27-4cdc-96db-03fba03ae58a)


   <h3 style="color: #34495e; margin-top: 15px;">Question 8: Which Corporate Customer placed the most number of orders in 2009 - 2012?</h3>
    <pre style="background-color: #ecf0f1; padding: 10px; border-radius: 5px; overflow-x: auto;"><code>SELECT Customer_Name, COUNT(DISTINCT Order_ID) AS Order_Count
FROM `job-tracker-462912.Capstone.capstone_corrected`
WHERE Customer_Segment = 'Corporate'
AND Order_Date BETWEEN '2009-01-01' AND '2012-12-31'
GROUP BY Customer_Name
ORDER BY Order_Count DESC
LIMIT 1;</code></pre>
    <p style="margin: 10px 0;"><b style="font-weight: bold;">Insight</b>: <span style="background-color: #ffeaa7; padding: 2px 5px; border-radius: 3px;">Grant Carroll</span> placed the most orders (15) among corporate customers during 2009-2012.</p>



![8](https://github.com/user-attachments/assets/96606876-a97e-475e-8ea1-a069ae6b2d57)



   <h3 style="color: #34495e; margin-top: 15px;">Question 9: Which consumer customer was the most profitable one?</h3>
    <pre style="background-color: #ecf0f1; padding: 10px; border-radius: 5px; overflow-x: auto;"><code>SELECT Customer_Name, SUM(Profit) AS Total_Profit
FROM `job-tracker-462912.Capstone.capstone_corrected`
WHERE Customer_Segment = 'Consumer' AND Profit IS NOT NULL
GROUP BY Customer_Name
ORDER BY Total_Profit DESC
LIMIT 1;</code></pre>
    <p style="margin: 10px 0;"><b style="font-weight: bold;">Insight</b>: <span style="background-color: #ffeaa7; padding: 2px 5px; border-radius: 3px;">Sally Hughsby</span> was the most profitable consumer customer, with a total profit of <b style="font-weight: bold;">$19,000</b>.</p>


![9](https://github.com/user-attachments/assets/27d0b06a-4b51-41cd-9424-2262eff96327)



   <h3 style="color: #34495e; margin-top: 15px;">Question 10: Which customer returned items, and what segment do they belong to?</h3>
    <pre style="background-color: #ecf0f1; padding: 10px; border-radius: 5px; overflow-x: auto;"><code>SELECT DISTINCT Customer_Name, Customer_Segment
FROM `job-tracker-462912.Capstone.capstone_corrected`
WHERE Profit < 0;</code></pre>
    <p style="margin: 10px 0;"><b style="font-weight: bold;">Insight</b>: Customers like <span style="background-color: #ffeaa7; padding: 2px 5px; border-radius: 3px;">Muhammed MacIntyre</span> (Small Business), <span style="background-color: #ffeaa7; padding: 2px 5px; border-radius: 3px;">Sylvia Foulston</span> (Home Office), and <span style="background-color: #ffeaa7; padding: 2px 5px; border-radius: 3px;">Jim Radford</span> (Corporate) returned items.</p>

  <h3 style="color: #34495e; margin-top: 15px;">Question 11: If the delivery truck is the most economical but the slowest shipping method and Express Air is the fastest but the most expensive one, do you think the company appropriately spent shipping costs based on the Order Priority? Explain your answer.</h3>
    <pre style="background-color: #ecf0f1; padding: 10px; border-radius: 5px; overflow-x: auto;"><code>SELECT Order_Priority, Ship_Mode, COUNT(*) AS Frequency
FROM `job-tracker-462912.Capstone.capstone_corrected`
GROUP BY Order_Priority, Ship_Mode
ORDER BY Order_Priority, Frequency DESC;</code></pre>
    <p style="margin: 10px 0;"><b style="font-weight: bold;">Insight</b>: KMS did not appropriately spend shipping costs, as critical and high-priority orders often used the slow Delivery Truck method, risking delays. Express Air should be prioritized for urgent orders to ensure timely delivery.</p>


![11,1](https://github.com/user-attachments/assets/0639b0ea-52ce-4e91-bcff-bd4e592fd33f)



![11,2](https://github.com/user-attachments/assets/b5b8e81f-231b-41b7-b12f-d322b4f5648a)




   <h2 style="color: #2980b9; margin-top: 20px;">Conclusion</h2>
    <p style="margin: 10px 0;">This project showcases my ability to work with large datasets, perform complex SQL queries, and derive actionable business insights. I cleaned and transformed the data, wrote queries to answer specific questions, and provided recommendations based on the findings. The project highlights my skills in data analysis, SQL, and business intelligence.</p>
   
</html>
