
# 🛒 Blinkit Sales & Operations Dashboard

**Interactive Business Intelligence Dashboard | Power BI • DAX • Data Visualization**

An interactive Power BI project designed to analyze Blinkit's sales performance, product categories, outlet operations, ratings, and location-tier distribution. This project includes three interactive dashboard pages with KPI cards, charts, tables, and slicers for business analysis.

---

## 📌 Project Overview

The objective of this project is to transform grocery sales data into meaningful business insights using Microsoft Power BI.

The dashboard helps explore the following business questions:

- 💰 What is the overall sales performance?
- ⭐ What is the average rating?
- 🏪 How do outlets perform across different outlet types and sizes?
- 🥦 Which product categories generate higher sales?
- 📈 How do sales change by outlet establishment year?
- 📍 How are sales distributed across location tiers?
- 👁️ What is the relationship between item visibility and sales?
- 🥛 How do sales vary by fat content?

## 📊 Key Performance Indicators (KPIs)

| KPI | Description |
|---|---|
| Total Sales | Total sales value under the selected filters |
| Average Rating | Average rating across the selected records |
| Total Outlets | Number of distinct outlets |
| Total Items | Item count based on the report measure |
| Total Categories | Number of distinct item categories |
| Average Visibility | Average item visibility |
| Average Item Weight | Average product weight |

*Note: KPI values may change when interactive slicers are applied.*

---

## 🖥️ Dashboard Pages

### 1. Overview

**Objective:** Provide an executive summary of sales and outlet performance.

**Key Visualizations:**
- Sales Trends by Establishment Year
- Sales by Outlet Type
- Sales by Item Category
- Top 5 Items by Sales and Average Rating
- Sales Distribution by Location Tier

**Key KPIs:**
- Total Sales
- Average Rating
- Total Outlets
- Total Items
- Total Categories

### 2. Product & Outlet Analysis

**Objective:** Analyze product attributes and sales performance across outlet characteristics.

**Key Visualizations:**
- Sales vs. Item Visibility
- Sales by Outlet Size
- Sales by Item Category
- Sales vs. Rating
- Sales Distribution by Fat Content

**Interactive Filters:**
- Year / Date
- Outlet Type
- Location Tier
- Outlet Size
- Fat Content

### 3. Outlet Performance

**Objective:** Compare outlet-level sales, ratings, and operational metrics.

**Key Visualizations:**
- Sales by Outlet Establishment Year
- Average Rating by Outlet Type
- Top Outlets by Total Sales
- Outlet Performance Summary Table

**Metrics Analyzed:**
- Average Rating
- Average Sales
- Total Sales
- Total Items
- Average Visibility

---

## 🗂️ Dataset

This project contains the following dataset files:

- `BlinkIT-Grocery-Data_Clean.xlsx` — Cleaned grocery sales dataset
- `BlinkIT-Grocery-Data_Raw.csv` — Raw grocery sales dataset

The report analyzes fields related to:

| Field | Description |
|---|---|
| Item Type | Product category |
| Item Weight | Product weight |
| Item Visibility | Product visibility value |
| Fat Content | Product fat-content classification |
| Sales | Sales value |
| Rating | Rating field used in the report |
| Outlet Identifier | Unique outlet identifier |
| Outlet Establishment Year | Year the outlet was established |
| Outlet Size | Outlet size category |
| Outlet Location Type | Outlet location classification |
| Outlet Type | Outlet format or type |

*Use the actual column names from the Power BI data model if they differ from these labels.*

---

## 📐 DAX Measures

The following DAX examples illustrate the calculations used for the dashboard. Replace `BlinkIT` with the actual table name in your Power BI model if necessary.

### 💰 Total Sales

```dax
Total Sales =
SUM ( BlinkIT[Sales] )
```

### ⭐ Average Rating

```dax
AVG RATING =
AVERAGE ( BlinkIT[Rating] )
```

### 🏪 Total Outlets

```dax
TOTAL OUTLETS =
DISTINCTCOUNT ( BlinkIT[Outlet Identifier] )
```

### 🛍️ Total Items

If the measure is intended to count dataset rows:

```dax
TOTAL ITEMS =
COUNTROWS ( BlinkIT )
```

If you want to count unique products, use `DISTINCTCOUNT` on the appropriate product identifier or product-name column.

### 🗂️ Total Categories

```dax
TOTAL CATEGORIES =
DISTINCTCOUNT ( BlinkIT[Item Type] )
```

### 👁️ Average Visibility

```dax
AVG VISIBILITY =
AVERAGE ( BlinkIT[Item Visibility] )
```

### ⚖️ Average Item Weight

```dax
AVG ITEM WEIGHT =
AVERAGE ( BlinkIT[Item Weight] )
```

### 💵 Average Sales

```dax
AVG SALES =
AVERAGE ( BlinkIT[Sales] )
```

**Important:** These are example formulas. Verify the table name, column names, and intended calculation before using them in your report.

---

## 🎨 Dashboard Design & Color Palette

The dashboard follows a Blinkit-inspired visual theme using yellow, cream, olive, and charcoal colors.

| Element | Hex Code |
|---|---|
| Primary Yellow | `#FCE006` |
| Cream Background | `#F5F0D1` |
| Card Background | `#FFFDF5` |
| Charcoal Text / Sidebar | `#29291F` |
| Olive Accent | `#77752B` |
| Muted Gold | `#B7AD64` |
| Borders / Gridlines | `#E8E2C9` |

**Design Principles:**
- Yellow highlights important KPIs and active navigation.
- Cream and off-white backgrounds maintain readability.
- Charcoal provides strong text contrast.
- Olive and muted gold create visual consistency across charts.
- Consistent formatting is applied across all three dashboard pages.

---

## 📊 Visualizations Used

- **KPI Cards:** Total Sales, Average Rating, Total Outlets, Total Items, and Total Categories
- **Line / Area Charts:** Sales trends by outlet establishment year
- **Bar Charts:** Sales by item category and outlet identifier
- **Column Charts:** Sales or ratings by outlet type and outlet size
- **Donut Charts:** Sales distribution by location tier and fat content
- **Scatter Charts:** Sales vs. item visibility and rating
- **Tables / Matrices:** Outlet-level performance comparison
- **Slicers:** Year / Date, Outlet Type, Location Tier, Outlet Size, and Fat Content

---

## 🔄 Project Workflow

1. Load the raw grocery sales dataset.
2. Review and clean the data using Excel or Power Query.
3. Verify column names and data types.
4. Create DAX measures for KPIs and sales analysis.
5. Build interactive charts, tables, and KPI cards.
6. Apply a consistent Blinkit-inspired color theme.
7. Configure slicers and cross-filtering.
8. Validate totals, labels, and calculations.
9. Save the final Power BI report.

---

## 💡 Business Analysis Opportunities

### Sales Performance
Compare sales across outlet types, outlet sizes, and establishment years.

### Product Category Analysis
Identify product categories with higher and lower sales contributions.

### Outlet Performance
Compare outlets using total sales, average sales, ratings, and item counts.

### Rating Analysis
Explore rating patterns across outlet types and compare ratings with sales.

### Item Visibility Analysis
Investigate the relationship between product visibility and sales.

### Location Tier Analysis
Compare sales distribution across different outlet location tiers.

### Fat Content Analysis
Explore sales distribution between fat-content groups.

*These are analysis opportunities. Actual conclusions should be based on the data and selected filters.*

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Microsoft Power BI | Dashboard development and visualization |
| DAX | Measures and KPI calculations |
| Power Query | Data transformation and preparation |
| Microsoft Excel | Dataset preparation |
| CSV | Raw dataset format |

---

## 📚 Skills Demonstrated

- Power BI Dashboard Development
- DAX Measure Creation
- Data Cleaning and Transformation
- KPI Design
- Data Visualization
- Sales and Outlet Performance Analysis
- Interactive Slicers and Cross-Filtering
- Dashboard Layout and Visual Consistency
- Business Intelligence
- Data Storytelling

---

## 📁 Project Structure

```text
Blinkit-Sales-Operations-Dashboard/
│
├── Datasets/
│   ├── BlinkIT-Grocery-Data_Clean.xlsx
│   └── BlinkIT-Grocery-Data_Raw.csv
│
├── Documentation/
│   └── Blinkit_Sales_Operations_Dashboard_Documentation.pdf
│
├── Images/
│   ├── Delivery.png
│   ├── Home.png
│   ├── Logo.jpg
│   ├── Outlet.png
│   ├── Profit.png
│   ├── Store.png
│   └── Store_Shares.png
│
├── Screenshots/
│   ├── Outlet Performance.png
│   ├── Overview.png
│   └── Product & Outlet Analysis.png
│
├── Blinkit_Analysis.pbix
└── README.md
```

---

## 📸 Dashboard Preview

### 🏠 Overview

![Blinkit Overview](Screenshots/Overview.png)

### 🛍️ Product & Outlet Analysis

![Product & Outlet Analysis](Screenshots/Product%20%26%20Outlet%20Analysis.png)

### 🏪 Outlet Performance

![Outlet Performance](Screenshots/Outlet%20Performance.png)

---

## 📄 Project Documentation

Detailed project documentation is available in the `Documentation` folder.

**[📥 View Project Documentation (PDF)](Documentation/Blinkit_Sales_Operations_Dashboard_Documentation.pdf)**

The documentation covers:
- Project overview and objectives
- Dashboard pages and visualizations
- KPI definitions
- Example DAX measures
- Design and color palette
- Project structure
- Quality checks and usage instructions

---

## 🚀 How to Use

1. Clone or download this repository.
2. Open `Blinkit_Analysis.pbix` in Microsoft Power BI Desktop.
3. If prompted, update the data-source path to the dataset location on your computer.
4. Refresh the report.
5. Explore the three dashboard pages using the interactive slicers and visuals.

---

## 🎯 Project Outcome

This project demonstrates how grocery sales data can be transformed into an interactive Power BI dashboard for analyzing sales performance, product categories, ratings, and outlet operations.

It showcases practical skills in data preparation, DAX calculations, KPI development, data visualization, and business-focused reporting.

---

## 👩‍💻 Author

**Chanchal Khandkure**

Aspiring Data Analyst

**Skills:** Power BI • SQL • Python • Excel • DAX • Data Analysis • Data Visualization

- GitHub: [Chanchal2011](https://github.com/Chanchal2011)

---

⭐ If you find this project useful, feel free to explore the dashboard and share feedback.
