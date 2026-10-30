<div align="center">

# 💊 Pharmaceutical Sales Performance Dashboard

### Transforming Pharmaceutical Sales Data into Actionable Insights

An interactive **Power BI dashboard** for analyzing pharmaceutical sales performance, exploring product contribution, and monitoring sales trends through clear, data-driven visualizations.

<br>

[![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=for-the-badge\&logo=powerbi\&logoColor=black)](https://powerbi.microsoft.com/)
[![DAX](https://img.shields.io/badge/DAX-Measures-1E99EA?style=for-the-badge)](https://learn.microsoft.com/en-us/dax/)

<br>

**Developed by Ahmed Khaled**

[LinkedIn](https://www.linkedin.com/in/ahmed-khaled-s/) • [GitHub](https://github.com/a7med-k4aled)

</div>

---

## 📌 Project Overview

The **Pharmaceutical Sales Performance Dashboard** is a business intelligence project developed using Microsoft Power BI to turn pharmaceutical sales data into meaningful business insights.

The dashboard helps explore recorded sales value, sales volumes, product performance, distributor contributions, regional distribution, and sales types through interactive visualizations.

The report is organized into three analytical pages, each focusing on a distinct business objective.

## 🎯 Project Objectives

* Monitor overall sales performance.
* Track sales value and recorded sales units.
* Identify top-performing pharmaceutical products.
* Compare sales across product lines.
* Analyze sales contributions by distributor and region.
* Explore the distribution of sales by sales type.
* Present key business metrics in a clean, interactive dashboard.

---

## 🖥️ Dashboard Preview

### 🏥 Cover Page

<img src="images/0-%20Page%20Cover.png" alt="Pharmaceutical Sales Dashboard Cover Page" width="100%"/>

*An introduction to the dashboard, its navigation, and its analytical sections.*

---

## 📊 Dashboard Pages

### 01 — Sales Performance Overview

<img src="images/1-%20Sales%20Overview.png" alt="Sales Performance Overview" width="100%"/>

Provides a high-level view of recorded sales performance.

**Key Metrics**

* Total Sales
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

* How does sales value change over time?
* Which product lines contribute most to sales?
* Which products generate the highest sales value?
* How are sales distributed across sales types?

---

### 02 — Product Analysis

<img src="images/2-%20Product%20Analysis.png" alt="Product Analysis" width="100%"/>

Focuses on product-level sales performance.

**Key Metrics**

* Total Products
* Total Sales
* Total Sales Units
* Top Product Sales

**Visualizations**

* Top 10 Products by Sales
* Sales by Product Line
* Top 10 Products by Sales Units

**Business Questions**

* Which products generate the highest sales value?
* Which products have the highest recorded sales volume?
* How do product lines contribute to sales?
* Do the products with the highest sales value also lead in units sold?

---

### 03 — Financial Performance

<img src="images/3-%20Financial%20Performance.png" alt="Financial Performance" width="100%"/>

Examines the financial side of recorded sales, focusing on sales value and its distribution.

**Key Metrics**

* Total Sales
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
* Which distributors contribute most to sales?
* How is sales value distributed across regions?
* Which sales types contribute most to recorded sales value?

> **Data note:** The dataset contains sales-related fields, but verified cost data is not assumed. Profit and net profit are not calculated without the required cost information.

---

## 🗂️ Dataset Description

The project uses pharmaceutical sales records covering **January–March 2025**.

The dataset includes fields that support sales, product, customer, distributor, regional, and sales-type analysis.

| Field               | Description                                  |
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

### Data Quality Considerations

* Missing customer identifiers may affect distinct customer counts.
* Negative sales values should be investigated to determine whether they represent returns, adjustments, or other transactions.
* The currency and definitions of financial fields should be confirmed before interpreting the results.
* Sales value alone is insufficient to calculate profit or net profit.

---

## 🛠️ Tools & Technologies

<div align="center">

<a href="https://powerbi.microsoft.com/">
  <img src="https://img.shields.io/badge/Power%20BI-Visualization-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" alt="Microsoft Power BI"/>
</a>
<a href="https://learn.microsoft.com/en-us/power-query/">
  <img src="https://img.shields.io/badge/Power%20Query-Data%20Preparation-1686C8?style=for-the-badge" alt="Power Query"/>
</a>
<a href="https://learn.microsoft.com/en-us/dax/">
  <img src="https://img.shields.io/badge/DAX-KPI%20Calculations-08B9B4?style=for-the-badge" alt="DAX"/>
</a>
<a href="https://git-scm.com/">
  <img src="https://img.shields.io/badge/Git-Version%20Control-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git"/>
</a>

</div>

| Technology                 | Purpose                                      |
| -------------------------- | -------------------------------------------- |
| Microsoft Power BI Desktop | Dashboard development and data visualization |
| Power Query                | Data preparation and transformation          |
| DAX                        | KPI calculations and analytical measures     |
| Git & GitHub               | Version control and project documentation    |

---

## 🧮 Selected DAX Measures

The following measures support the dashboard's core sales analysis.

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
    DISTINCTCOUNT('Q1 Sales Performance'[EGPI Product Name]),
    'Q1 Sales Performance'[EGPI Product Name] <> BLANK()
)
```

### Total Distributors

```dax
Total Distributors =
CALCULATE(
    DISTINCTCOUNT('Q1 Sales Performance'[DISTRIBUTOR]),
    'Q1 Sales Performance'[DISTRIBUTOR] <> BLANK()
)
```

*Note: The table name used above must match the actual table name in the Power BI data model.*

---

## 🎨 Dashboard Design

The dashboard uses a consistent healthcare-inspired color palette.

| Color  | Hex Code  | Purpose                                   |
| ------ | --------- | ----------------------------------------- |
| Blue   | `#1E99EA` | Primary visuals and navigation accents    |
| Teal   | `#08B9B4` | Secondary highlights                      |
| Orange | `#F28444` | Financial accents and selected highlights |

### Design Principles

* Consistent visual identity across all pages.
* Clear KPI cards for important metrics.
* Interactive slicers for exploring the data.
* Focused charts and minimal visual clutter.
* Consistent navigation and layout.
* Business-focused insights based on available data.

---

## 🎬 Project Demonstration

<div align="center">

### Watch the Dashboard in Action

**A short walkthrough of the Pharmaceutical Sales Performance Dashboard.**

<!-- Replace YOUR_LINKEDIN_POST_URL with the URL of your published LinkedIn post. -->

[![Watch the Project Demo](https://img.shields.io/badge/LinkedIn-Watch%20Project%20Demo-0A66C2?style=for-the-badge\&logo=linkedin\&logoColor=white)](YOUR_LINKEDIN_POST_URL)

**Video:** [View the full project demonstration on LinkedIn](YOUR_LINKEDIN_POST_URL)

</div>

> Replace `YOUR_LINKEDIN_POST_URL` in both locations above with the actual URL of your published LinkedIn post. The video itself is hosted on LinkedIn; GitHub provides a link to it.

---

## 👨‍💻 About the Author

<div align="center">

### Ahmed Khaled

**Aspiring Data Analyst | Power BI | SQL | Excel**

Interested in transforming raw data into meaningful insights through business intelligence, data visualization, and analytical problem-solving.

<br>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge\&logo=linkedin\&logoColor=white)](https://www.linkedin.com/in/ahmed-khaled-s/)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=for-the-badge\&logo=github\&logoColor=white)](https://github.com/a7med-k4aled)

</div>

---

<div align="center">

### Pharmaceutical Sales Performance Dashboard

**Turning Data into Insights.**

</div>
