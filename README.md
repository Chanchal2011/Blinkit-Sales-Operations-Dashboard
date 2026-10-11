# 🛒 Blinkit Sales & Operations Dashboard

**Interactive Business Intelligence Dashboard \| Power BI • DAX • Data
Visualization**

An interactive Power BI project analyzing Blinkit sales, product
categories, and outlet performance through KPI cards, trend analysis,
category comparisons, outlet-size analysis, ratings, and location-tier
distribution.

------------------------------------------------------------------------

## 📌 Project Overview

This project uses Microsoft Power BI to explore grocery sales and outlet
performance. The dashboard is designed to answer questions such as:

-   💰 What are the overall sales and average ratings?
-   🏪 How do outlets compare by outlet type, size, and identifier?
-   🥦 Which item categories contribute the most sales?
-   ⭐ How do ratings vary across outlet types?
-   📍 How are sales distributed across location tiers?
-   🥛 How does sales performance vary by fat content?
-   👁️ What is the relationship between item visibility and sales?

## 📊 Executive Snapshot

  KPI                          Description
  ---------------------------- ---------------------------------------------
  💰 Total Sales               Total sales value under the current filters
  ⭐ Average Rating            Average rating across the selected records
  🏪 Total Outlets             Number of distinct outlets
  🛍️ Total Items               Item count based on the measure definition
  🗂️ Total Categories          Number of distinct item categories
  👁️ Average Item Visibility   Average visibility value
  ⚖️ Average Item Weight       Average item weight

*Values can change when slicers are applied.*

## 🗂️ Dataset

Fields visible in the report include:

  -----------------------------------------------------------------------
  Field                               Description
  ----------------------------------- -----------------------------------
  Item Type                           Product category

  Item Weight                         Product weight

  Item Visibility                     Product visibility value

  Fat Content                         Product fat-content classification

  Sales                               Sales value

  Rating                              Rating field used in the report

  Outlet Identifier                   Outlet identifier

  Outlet Establishment Year           Year the outlet was established

  Outlet Size                         Outlet size category

  Outlet Location Type / Location     Outlet location classification
  Tier                                

  Outlet Type                         Outlet format/type
  -----------------------------------------------------------------------

*Use the exact column names from your Power BI model if they differ from
these labels.*

## 🖥️ Power BI Dashboard

The report contains three pages.

### 1️⃣ Overview

**Business objective:** Provide a high-level summary of sales and outlet
performance.

**Key KPIs** - Total Sales - Average Rating - Total Outlets - Total
Items - Total Categories

**Main analysis** - Sales trends by outlet establishment year - Sales by
outlet type - Sales by item category - Top items by sales and average
rating - Sales distribution by location tier

### 2️⃣ Product & Outlet Analysis

**Business objective:** Explore product attributes and compare sales
across outlet characteristics.

**Main analysis** - Sales versus item visibility - Sales by outlet
size - Sales by item type - Sales versus rating - Sales distribution by
fat content

**Interactive filters** - Year / Date - Outlet Type - Location Tier -
Outlet Size - Fat Content

### 3️⃣ Outlet Performance

**Business objective:** Compare outlet-level sales, ratings, visibility,
and item counts.

**Main analysis** - Sales by outlet establishment year - Average rating
by outlet type - Top outlets by total sales - Outlet performance summary
table - Comparison by average rating, average sales, total sales, total
items, and average visibility

## 📐 Core DAX Measures

The following examples align with the fields shown in the report. Update
table and column names to match your Power BI model.

### 💰 Total Sales

``` dax
Total Sales =
SUM ( BlinkIT[Sales] )
```

### ⭐ Average Rating

``` dax
AVG RATING =
AVERAGE ( BlinkIT[Rating] )
```

### 🏪 Total Outlets

``` dax
TOTAL OUTLETS =
DISTINCTCOUNT ( BlinkIT[Outlet Identifier] )
```

### 🛍️ Total Items

If each row represents an item record and you want to count rows:

``` dax
TOTAL ITEMS =
COUNTROWS ( BlinkIT )
```

If you want unique products, use the relevant product-name column
instead.

### 🗂️ Total Categories

``` dax
TOTAL CATEGORIES =
DISTINCTCOUNT ( BlinkIT[Item Type] )
```

### 👁️ Average Visibility

``` dax
AVG VISIBILITY =
AVERAGE ( BlinkIT[Item Visibility] )
```

### ⚖️ Average Item Weight

``` dax
AVG ITEM WEIGHT =
AVERAGE ( BlinkIT[Item Weight] )
```

### 💵 Average Sales

``` dax
AVG SALES =
AVERAGE ( BlinkIT[Sales] )
```

**Important:** `BlinkIT` is a placeholder table name. Replace it with
the exact table name in your model. Confirm whether `TOTAL ITEMS` should
count rows or unique products before publishing.

## 🎨 Dashboard Design

The dashboard uses a Blinkit-inspired yellow, cream, olive, and charcoal
palette.

  Element                   Color
  ------------------------- -----------
  Primary yellow            `#FCE006`
  Cream background          `#F5F0D1`
  Chart/card background     `#FFFDF5`
  Charcoal text / sidebar   `#29291F`
  Olive accent              `#77752B`
  Muted gold                `#B7AD64`
  Borders / gridlines       `#E8E2C9`

Yellow highlights important KPIs and active navigation. Cream and
off-white provide contrast, while charcoal and olive are used for text
and secondary chart elements.

## 📊 Dashboard Visualizations

-   **KPI cards:** Sales, rating, outlets, items, and categories
-   **Line chart:** Sales by outlet establishment year
-   **Bar / column charts:** Sales by outlet type, item category, outlet
    size, and outlet identifier
-   **Donut charts:** Sales distribution by location tier and fat
    content
-   **Scatter plots:** Sales versus item visibility and rating
-   **Matrix / table:** Outlet-level performance comparison
-   **Slicers:** Year/date, outlet type, location tier, outlet size, and
    fat content

## 🔄 Analytics Workflow

1.  Load the dataset into Power BI.
2.  Review and clean the data in Power Query.
3.  Check column names and data types.
4.  Create DAX measures for sales, ratings, outlets, items, and
    categories.
5.  Build KPI cards and interactive visuals.
6.  Apply consistent colors and formatting across all three pages.
7.  Test slicers and cross-filtering.
8.  Validate totals and labels before publishing.

## 💡 Analysis Opportunities

1.  **Sales performance:** Compare sales across outlet types, outlet
    sizes, and establishment years.
2.  **Product categories:** Identify categories with higher and lower
    sales.
3.  **Outlet comparison:** Compare outlets by total sales, average
    sales, ratings, and item counts.
4.  **Rating patterns:** Review average ratings by outlet type and
    compare ratings with sales.
5.  **Product visibility:** Explore the relationship between item
    visibility and sales.
6.  **Location distribution:** Compare sales across location tiers.
7.  **Fat content:** Compare sales distribution between fat-content
    groups.

These are analysis questions supported by the dashboard; conclusions
should be drawn from the actual data and selected filters.

## 🛠️ Tech Stack

  Area                        Technology
  --------------------------- --------------------
  Data visualization          Microsoft Power BI
  Data transformation         Power Query
  Measures and calculations   DAX
  Business intelligence       Power BI
  Dashboard design            Power BI

## 📚 Skills Demonstrated

-   Power BI report development
-   DAX measure creation
-   Data cleaning and transformation
-   KPI design
-   Data visualization
-   Sales and outlet performance analysis
-   Interactive slicers and cross-filtering
-   Dashboard design and visual consistency
-   Business-focused data storytelling

## 📁 Project Structure

``` text
Blinkit-Sales-Operations-Dashboard/
│
├── README.md
├── Blinkit_Sales_Operations_Dashboard.pbix
├── Screenshots/
│   ├── Overview.png
│   ├── Product-Outlet-Analysis.png
│   └── Outlet-Performance.png
└── Dataset/
    └── dataset.csv
```

*Keep only the folders and files you actually add to your repository.
Share the dataset only if its license permits redistribution.*

## 📸 Dashboard Preview

Add screenshots to the `Screenshots/` folder and update these image
links:

```{=html}
<!--
### Overview
![Blinkit Overview](Screenshots/Overview.png)

### Product & Outlet Analysis
![Product and Outlet Analysis](Screenshots/Product-Outlet-Analysis.png)

### Outlet Performance
![Outlet Performance](Screenshots/Outlet-Performance.png)
-->
```
## 🚀 How to Use

1.  Download or clone this repository.
2.  Open `Blinkit_Sales_Operations_Dashboard.pbix` in Microsoft Power BI
    Desktop.
3.  If prompted, update the data-source path to your local dataset.
4.  Refresh the report and interact with the slicers and visuals.

## 🎯 Project Outcome

This project demonstrates how a grocery sales dataset can be turned into
an interactive Power BI report for exploring sales, product categories,
ratings, and outlet performance. It showcases practical dashboard
development, DAX calculations, and business-oriented visual
storytelling.

## 👩‍💻 Author

**Chanchal Khandkure**\
Aspiring Data Analyst

**Skills:** Power BI • SQL • Python • Excel • Data Analysis • Data
Visualization

-   GitHub: [Chanchal2011](https://github.com/Chanchal2011)
-   LinkedIn: [Chanchal
    Khandkure](https://www.linkedin.com/in/chanchal-khandkure)

------------------------------------------------------------------------

⭐ If you find this project useful, feel free to explore the report and
share feedback.
