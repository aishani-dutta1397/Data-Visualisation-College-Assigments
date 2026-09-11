# Mini Projects 1 to 4

This repository contains four exploratory data analysis and dashboard visualization projects. The summaries below cover exoplanet observations, chocolate sales metrics, global search trends, and historical stock market trends.

## MiniProject1: Planetary Data Dashboard

### Dataset

The exoplanet analysis includes two versions of the data. `Raw.csv` contains **5,986 records and 10 columns**: planet name, planet status, mass, mass uncertainty bounds, minimum mass (`mass_sini`), minimum-mass uncertainty bounds, radius, and radius uncertainty. The raw file contains **28,234 missing cells**, preserving original observations where every raw record is labeled `Confirmed` in the available `planet_status` field.

`Cleaned_Exoplanet_Data_Final.csv` contains **3,062 records and 8 fully populated columns**: planet name, mass, mass uncertainty bounds, minimum-mass uncertainty bounds, radius, and radius uncertainty. The cleaned file removes `planet_status` and `mass_sini`, resolving missing values to provide a consistent numerical table.

### Visualizations

| Visualization | Dataset role | Purpose |
| --- | --- | --- |
| Number of Planets by Planet Status | Raw dataset | Shows the distribution of planets by status, dominated by the `Confirmed` category. |
| Top 10 Planets by Mass | Cleaned dataset | Ranks the ten planets with the highest recorded mass. |
| Relationship Between Planet Mass and Radius | Cleaned dataset | Uses a scatter plot to examine mass–radius correlation and highlight outliers. |

### Key Findings

The raw status field shows a dataset dominated by confirmed planets. Cleaned numerical figures reveal a heavily right-skewed mass distribution where a small group of planets is substantially more massive than the rest. The mass–radius scatter plot exhibits a dense cluster of low-mass, smaller-radius planets alongside a few extreme outliers.

---

## MiniProject2: Chocolate Sales Dashboard

### Dataset

The second project examines chocolate sales transactions across products, sales amounts, shipment box counts, cost per box, sales teams, and international geographic regions.

### Visualizations

| Visualization | Purpose |
| --- | --- |
| Sum of Amount by Product | Compares total sales revenue across chocolate products. |
| Sum of Boxes by Product | Compares sales and shipment volume by product. |
| Sum of Boxes by Team | Displays box volume distribution across sales teams. |
| Sum of Cost per Box by Product | Evaluates unit production and handling costs per item. |
| Geographic Map | Plots sales distribution across global markets. |
| Team and Geography Filters | Enables interactive slicing across regions and teams. |

### Key Findings

A handful of items drive a disproportionate share of volume and revenue, led by Peanut Butter Cubes, Milk Bars, and Eclairs. Box volumes are distributed evenly across sales teams without single-team dominance. Disparities in cost per box point to varying unit profit margins across product lines.

---

## MiniProject3: Google Search Trends Analysis

### Dataset

The analysis is performed on `trends.csv`, tracking search rankings from 2001 to 2020.

* **Initial Dimensions**: 26,955 rows and 5 columns (`location`, `year`, `category`, `rank`, `query`).


* **Data Integrity**: 0 null values across all attributes.


* **Deduplication**: 10 duplicate rows were identified and removed in-place, yielding a final set of 26,945 unique entries.


* **Categorical Breadth**: Contains 83 unique locations, 20 distinct years, 2,450 categories, and 18,431 unique query terms with ranks spanning 1 through 5.



### Exploration Summary

| Step | Method / Operation | Outcome |
| --- | --- | --- |
| Structure Inspection | `df.info()`, `df.dtypes` | Verified column data types: 2 integer fields (`year`, `rank`) and 3 object fields (`location`, `category`, `query`).

 |
| Missing Value Check | `df.isnull().sum()` | Confirmed complete completeness with zero null values across all columns.

 |
| Duplicate Handling | `df.drop_duplicates()` | Cleaned 10 redundant rows to ensure exact uniqueness.

 |
| Cardinality Analysis | `df.nunique()` | Summarized geographical, temporal, and topical coverage across global search topics.

 |

### Key Findings

The dataset offers a balanced top-5 ranking structure (mean rank: 3.0, median: 3.0) across two decades of query history. The high volume of unique categories (2,450) relative to total rows demonstrates significant thematic variety across cultural and regional search behaviors.

---

## MiniProject4: Historical Stock Prediction & OHLC Analysis

### Dataset

The fourth project analyzes long-term historical trading movements across three major equities: **Apple (AAPL)**, **Google (GOOGL)**, and **Tesla (TSLA)**. The data models Open, High, Low, Close (OHLC), and Volume metrics across multi-year intervals using interactive date slicers.

### Visualizations

| Stock Dashboard | Visualizations Included | Timeframe Analyzed |
| --- | --- | --- |
| Apple Stock Analysis | Line charts of Sum of Close and Sum of Open by Date; Scatter plot of Open vs. Close; Date Slicer

 | 12-12-1980 to 02-03-2000

 |
| Google Stock Analysis | Line charts of Sum of Close and Sum of Open by Year; Scatter plot of Open vs. Close; Date Slicer

 | 19-08-2004 to 01-04-2020

 |
| Tesla Stock Analysis | Line charts of Sum of Close and Sum of Open by Year; Scatter plot of Open vs. Close; Date Slicer

 | 29-06-2010 to 01-04-2020

 |

### Key Findings

* **Tight Intraday Linearity**: Across all three assets, Open vs. Close scatter plots show tight 45-degree linear paths, indicating that opening trade values heavily dictate end-of-day closes with contained daily swings.


* **Apple Dot-Com Run-Up**: Apple hovered between 0 and 2 from 1980 until approximately 1998, followed by a vertical surge past 4 heading into 2000 during the dot-com bubble. A single isolated outlier dot sits apart from the primary diagonal corridor.


* **Google Bull Market**: Showed continuous compound growth from late 2004 onward, accelerating sharply after 2012 and peaking in 2019. Points clump closely under 1,500, showing wider dispersion at peak valuations.


* **Tesla Volatility**: Demonstrates an early rally between 2012 and 2014 before reaching peak aggregate levels near 80K during 2017–2018. Higher-value regimes ($600–$900) show wider scatter dispersion than Apple or Google, demonstrating heightened volatility.


* **2020 Partial Data Truncation**: Sharp visual drop-offs in the 2020 charts for Google and Tesla stem from an April 1, 2020 data cutoff, representing only one quarter of trading volume against 12-month historical totals.



---

## Source Files

| File | Description |
| --- | --- |
| `MiniProject1.xlsx` | Exoplanet dashboard containing planet status distributions, mass rankings, and mass–radius scatter plots. |
| `MiniProject2.pdf` | Chocolate sales dashboard tracking revenue, team distribution, unit box costs, and regional performance. |
| `DV_trends_dataset_Aishani-Copy1.pdf` | Jupyter notebook detailing data cleaning, schema validation, and profiling of `trends.csv`.

 |
| `Mini_Project_4_Aishani.pdf` | Power BI / visualization report exploring OHLC trends, intraday spreads, and multi-year trajectory analyses for Apple, Google, and Tesla.

 |
