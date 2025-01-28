
# PowerBI Data Analysis

## BlinkIT Sales Analysis

### Table of Contents

- [Project Description](#project-description)
- [Data Source](#data-source)
- [Data Cleaning](#data-cleaning)
- [Tools](#tools)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data Analysis](#data-analysis)
- [Results/Findings](#resultsfindings)
  

### Project Description
The project aims to create a comprehensive dashboard to analyze the blinkIT sales analysis. We have analyzed the data based on fat content available in the product, item types, outlet establishment year, store size, and region. It is a dynamic dashboard where we can filter out the option to perform deep-dive analysis.

![BlinkIT Grocey Sales Dashboard image](BlinkIT%20Sales%20Analysis.png)

### Data Source
- BlinkIT Sales Data: The data is available in the "BlinkIT Grocery Data.xlsx" file which contains all the data related to its sales, items available, and products with the fat content.

### Tools
- Power BI Desktop: For data cleaning and visualization.

### Data Cleaning
- In the Power BI Desktop, we have inserted the xlsx data. I have checked each column for missing values and formatting issues. I have also checked whether the datatypes assigned to each column are correct. I have replaced the fat outlet from the abbreviation to its full form for proper analysis.

### Exploratory Data Analysis
Performed some exploratory data analysis to find some information about key questions like
- Total Sales, Average Sales, Orders placed, and the rating as major KPIs.
- Sales, rating, average sales, and orders placed by fat outlet.
- Sales, rating, average sales, and order by item types.
- Which outlet is performing better sales by the outlet establishment?
- Which outlet size and region is performing better sales?
  

### Data Analysis
To find the answer to the key questions, I have written some query in the MySQL as
``` PowerBI
Total Sales = SUM('BlinkIT Grocery Data'[Sales])
```
``` PowerBI
# Creation of Parameter
Metrics = {
    ("Total Sales", NAMEOF('BlinkIT Grocery Data'[Total Sales]), 0),
    ("Average Sales", NAMEOF('BlinkIT Grocery Data'[Average Sales]), 1),
    ("No of Items", NAMEOF('BlinkIT Grocery Data'[No of Items]), 2),
    ("Average Rating", NAMEOF('BlinkIT Grocery Data'[Average Rating]), 3)
}
```

### Results/Findings
- The total sale is around $1.20M and the average sale is around $141.
- Low-fat content products perform better than regular fat-content products.
- Fruits and Vegetables and snacks food are generating maximum sales.
- The outlet that was established in the year 2018 is generating high revenue as compared to others.
- Medium outlet size and Tier 3 regions are generating better revenue.
