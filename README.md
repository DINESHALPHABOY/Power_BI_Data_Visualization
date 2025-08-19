# Power BI Reports – Data Analysis & Insights

This repository contains **Power BI reports** designed to analyze, visualize, and present insights from different datasets. The goal is to provide clean and interactive dashboards that help in decision-making using data-driven approaches.  

---

## Features
- Interactive dashboards with filters and slicers  
- Visualizations for trend analysis, KPIs, and drill-throughs  
- Reports built with **Power BI Desktop**  
- Example datasets for testing and practice  

---

## Repository Structure

**Sales Performance**
talks about the Sales Performance in Retail-Sales Dataset
- Top Sales by Quality
- Product Category by Highest Revenue
- Total Revenue over a period of time
- *Measures* : Total Revenue, Quarterly Revenue and Yearly Revenue

<img width="1170" height="652" alt="Sales Performance" src="https://github.com/user-attachments/assets/990abf95-0636-498c-bfd9-4f619c0f0be6" />

---

**Customer Behavior**
tells about the behavior of the Customers by Gender and Age Categories
- Total Revenue by Age Group
- Average Age of Customers per Category
- Average Transactions per Customers
- *Measures* : Unique Customers, Total Revenue, Total Transactions and Average Revenue
<img width="1172" height="651" alt="Customer Behavior " src="https://github.com/user-attachments/assets/1b005589-cd06-409d-bb48-4eae04e04ddc" />

---

**Product Analysis, Segmentation and Targetting**
has an analysed visualizes of products, it segments the product based on Category, Gender and Age Group. The Targetting targets on the specific insights to increase profit(sales).
- Highest Average Unit Price by Product category
- Product Category based on Quantity Sold
- Most Expensive Purchase by Age and Gender
- Average Transaction by customer
- Product category Preference by Gender
<img width="1173" height="650" alt="Product Analysis, Segmentation   Targeting" src="https://github.com/user-attachments/assets/eb944ac8-0fa9-4cd0-8c49-97ffd36f5827" />


---

## DAX Queries   

### Total Revenue
```DAX 
Total Revenue = SUM('retail_sales_dataset'[Revenue])
```

### Quarterly Revenue
```DAX
Total Revenue Quarterly = CALCULATE([Total Revenue],DATESINPERIOD('retail_sales_dataset'[Date],MAX('retail_sales_dataset'[Date]),-1,QUARTER))
```

### Yearly Revenue
```DAX
Total Revenue Yearly = CALCULATE([Total Revenue],DATESINPERIOD('retail_sales_dataset'[Date],MAX('retail_sales_dataset'[Date]),-1,YEAR))
```

### Total Transaction
```DAX
Total Transactions = DISTINCTCOUNT('retail_sales_dataset'[Transaction ID])
```

### Average Revenue per Gender
```DAX
Total Revenue average per Gender = 
AVERAGEX(
	KEEPFILTERS(VALUES('retail_sales_dataset'[Gender])),
	CALCULATE([Total Revenue])
)
```

### Average Revenue
```DAX
Average Revenue = AVERAGE('retail_sales_dataset'[Revenue])
```


---


## Power Point - Background
I created the background for this Visualization using MS PowerPoint 
<img width="1280" height="720" alt="1" src="https://github.com/user-attachments/assets/9ac714c0-f8a2-4ff2-968e-d5b486bdba51" />
<img width="1280" height="720" alt="2" src="https://github.com/user-attachments/assets/a71df623-dacd-46fa-b2a4-5e3ae86ffb29" />


---

## How to use
- Import the retail_sales_dataset into Power BI.
- Add these DAX queries in the Modeling → New Measure section.
- Use them in cards, visuals, and dashboards to monitor revenue trends.
- Add Background, Go styling your Canvas !


---

# Tools used
- Power BI
- Power Point
- DAX Queries


---

# Author
*K N Dinesh Kumar*
*dineshdhieraj02@gmail.com*
