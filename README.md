<div align="center">

# 💊 Pharmaceutical Sales Performance Dashboard

### Transforming Pharmaceutical Sales Data into Actionable Insights

An interactive **Power BI dashboard** designed to analyze pharmaceutical sales performance, explore product contribution, and monitor financial sales trends through clear, data-driven visualizations.

<br>

![Power BI](https://img.shields.io/badge/Power%20BI-Analytics-F2C811?style=for-the-badge\&logo=powerbi\&logoColor=black)
![Microsoft Excel](https://img.shields.io/badge/Microsoft%20Excel-Data%20Source-217346?style=for-the-badge\&logo=microsoftexcel\&logoColor=white)
![Data Analytics](https://img.shields.io/badge/Data-Analytics-1E99EA?style=for-the-badge)
![Status](https://img.shields.io/badge/Project-Completed-08B9B4?style=for-the-badge)

<br>

**Developed by Ahmed Khaled**

[LinkedIn](https://www.linkedin.com/in/ahmed-khaled-s/) • [GitHub](https://github.com/a7med-k4aled)

</div>

---

## 📌 Project Overview

The **Pharmaceutical Sales Performance Dashboard** is a business intelligence project built with Microsoft Power BI to transform pharmaceutical sales data into meaningful business insights.

The project focuses on understanding sales performance, identifying top-performing products, and analyzing sales value across different periods, distributors, regions, and sales types.

Through interactive visualizations and KPI cards, the dashboard provides a clear overview of the dataset and supports data-driven exploration of pharmaceutical sales performance.

The dashboard is organized into three focused pages, each designed to answer a different set of business questions.

---

## 🎯 Project Objectives

* Monitor overall pharmaceutical sales performance.
* Track sales value and sales units.
* Identify products contributing the most to sales.
* Compare sales performance across product lines.
* Analyze sales distribution by distributor and region.
* Understand the contribution of different sales types.
* Provide an interactive and visually consistent reporting experience.

---

## 🖥️ Dashboard Preview

<!-- Replace these paths with your actual screenshot filenames. -->

<div align="center">

### Dashboard Cover

<img src="images/Cover.png" alt="Pharmaceutical Sales Dashboard Cover" width="100%"/>

*An overview of the dashboard design and navigation.*

</div>

---

## 📊 Dashboard Pages

### 01 — Sales Performance Overview

The main page provides a high-level overview of pharmaceutical sales performance.

**Key Metrics**

* Total Sales Value
* Total Sales Units
* Total Customers
* Total Products
* Total Distributors

**Visualizations**

* Monthly Sales Trend
* Sales by Product Line
* Sales by Sales Type
* Top 5 Products by Sales

**Business Questions**

* How much sales value was recorded during the reporting period?
* How did sales change from month to month?
* Which product lines contributed most to sales?
* Which products generated the highest sales value?
* How were sales distributed across different sales types?

<div align="center">

<img src="images/Sales_Overview.png" alt="Sales Performance Overview" width="100%"/>

</div>

---

### 02 — Product Analysis

This page focuses on product-level performance and helps identify the products that contribute most to overall sales.

**Key Metrics**

* Total Products
* Total Sales Value
* Total Sales Units
* Top Product Sales

**Visualizations**

* Top 10 Products by Sales
* Sales by Product Line
* Top 10 Products by Sales Units

**Business Questions**

* Which products generate the highest sales value?
* Which products account for the largest sales volumes?
* How do different product lines contribute to sales?
* Do the products with the highest sales value also lead in units sold?

<div align="center">

<img src="images/Product_Analysis.png" alt="Product Analysis Dashboard" width="100%"/>

</div>

---

### 03 — Financial Performance

This page examines the financial side of recorded sales, focusing on sales value rather than unverified profit or cost figures.

**Key Metrics**

* Total Sales Value
* Average Sales Value
* Highest Monthly Sales
* Sales Contribution Percentage

**Visualizations**

* Monthly Sales Trend
* Sales by Distributor
* Sales by Region
* Sales by Sales Type

**Business Questions**

* How does recorded sales value change over time?
* Which distributors contribute the most to sales?
* How is sales value distributed across regions?
* Which sales types contribute most to the recorded sales value?

> **Note:** The available dataset contains sales information, but verified cost data is not assumed. Profit and net profit are therefore not presented as calculated metrics.

<div align="center">

<img src="images/Financial_Performance.png" alt="Financial Performance Dashboard" width="100%"/>

</div>

---

## 🗂️ Dataset Description

The project uses pharmaceutical sales data covering the first quarter of 2025.

The dataset includes sales records and business dimensions that support product, customer, distributor, regional, and financial sales analysis.

### Key Fields

| Column              | Description                                  |
| ------------------- | -------------------------------------------- |
| `Month`             | Reporting month                              |
| `DISTRIBUTOR`       | Distributor associated with the sales record |
| `CUSTOMER NAME`     | Customer name                                |
| `CUSTOMER CODE`     | Customer identifier, where available         |
| `Territory`         | Sales territory                              |
| `REGION`            | Sales region                                 |
| `Line Name`         | Product line                                 |
| `EGPI Product Name` | Pharmaceutical product name                  |
| `SALES UNITS`       | Recorded sales units                         |
| `P Price`           | Recorded product price                       |
| `SALES VALUE`       | Recorded sales value                         |
| `SALES TYPE`        | Sales category                               |

The dataset is used to build interactive measures and visualizations within Power BI.

**Data considerations**

* Missing customer identifiers may affect distinct customer counts.
* Negative sales values should be investigated to determine whether they represent returns, adjustments, or other transactions.
* The currency and business definition of sales fields should be confirmed before interpreting financial figures.
* Sales value alone does not provide enough information to calculate profit or net profit.

---

## 🛠️ Tools & Technologies

| Tool                       | Purpose                                   |
| -------------------------- | ----------------------------------------- |
| Microsoft Power BI Desktop | Dashboard development and visualization   |
| Power Query                | Data preparation and transformation       |
| DAX                        | Measures and KPI calculations             |
| Microsoft Excel            | Source data storage and inspection        |
| Git & GitHub               | Version control and project documentation |

---

## 🧮 Key DAX Measures

The dashboard uses DAX measures to calculate sales KPIs and support interactive analysis.

### Total Sales

```dax
Total Sales =
SUM('Q1 Sales Performance'[SALES VALUE])
```

### Total Sales Units

```dax
Total Sales Units =
SUM('Q1 Sales Performance'[SALES UNITS])
```

### Total Products

```dax
Total Products =
CALCULATE(
    DISTINCTCOUNT(
        'Q1 Sales Performance'[EGPI Product Name]
    ),
    'Q1 Sales Performance'[EGPI Product Name] <> BLANK()
)
```

### Total Distributors

```dax
Total Distributors =
CALCULATE(
    DISTINCTCOUNT(
        'Q1 Sales Performance'[DISTRIBUTOR]
    ),
    'Q1 Sales Performance'[DISTRIBUTOR] <> BLANK()
)
```

*Note: These measures use the model table name shown above. Replace it if the table has a different name in your Power BI file.*

---

## 🎨 Design & User Experience

The dashboard follows a clean, healthcare-inspired visual identity designed to make the information easy to navigate and interpret.

### Color Palette

| Color  | Hex Code  | Usage                            |
| ------ | --------- | -------------------------------- |
| Blue   | `#1E99EA` | Primary visual elements          |
| Teal   | `#08B9B4` | Secondary accents                |
| Orange | `#F28444` | Highlights and financial accents |

### Design Principles

* Consistent colors across dashboard pages.
* Clear KPI cards for important metrics.
* Interactive filters for exploring sales data.
* Focused visualizations with minimal clutter.
* Consistent navigation and page structure.
* Business-oriented analysis instead of unnecessary complexity.

---

## 💡 Key Analytical Areas

The dashboard supports exploration of several important business dimensions:

**Sales Performance**
Monitor recorded sales value and unit volumes over time.

**Product Performance**
Identify high-performing products and compare product lines.

**Distributor Analysis**
Compare recorded sales contributions across distributors.

**Regional Analysis**
Explore the distribution of sales value across regions.

**Sales Type Analysis**
Compare sales contributions by recorded sales category.

These analytical areas help users explore the available data and investigate patterns without assuming that the observed relationships establish causation.

---

## 🚀 How to Use the Project

1. Download or clone this repository.
2. Locate the Power BI `.pbix` file.
3. Open it using Microsoft Power BI Desktop.
4. Interact with the available filters and visualizations.
5. Explore the three dashboard pages to examine sales, product, and financial performance.

If the original source data is not included in the repository, you may need authorized access to the dataset to refresh the report.

---

## 📁 Repository Structure

```text
Pharmaceutical-Sales-Performance-Dashboard/
│
├── README.md
│
├── Pharmaceutical Sales Dashboard.pbix
│
├── images/
│   ├── Cover.png
│   ├── Sales_Overview.png
│   ├── Product_Analysis.png
│   └── Financial_Performance.png
│
└── Documentation/
    └── Project_Overview.pdf
```

*This is the intended structure. Update filenames and remove entries for files that are not included in the repository.*

---

## 🔮 Future Improvements

Potential improvements include:

* Validating negative sales records and documenting the treatment of returns or adjustments.
* Improving data quality checks for missing customer identifiers.
* Adding year-over-year comparisons when historical data becomes available.
* Expanding the analysis when verified cost or margin data is available.
* Improving report documentation and adding additional validated business metrics.

---

## 👨‍💻 Author

<div align="center">

### Ahmed Khaled

**Aspiring Data Analyst | Power BI | SQL | Excel**

I enjoy transforming raw data into clear visualizations and actionable business insights through data analysis and business intelligence tools.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge\&logo=linkedin)](https://www.linkedin.com/in/ahmed-khaled-s/)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=for-the-badge\&logo=github)](https://github.com/a7med-k4aled)

</div>

---

<div align="center">

**Pharmaceutical Sales Performance Dashboard**

*Turning Data into Insights.*

</div>
