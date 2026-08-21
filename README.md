# Mini Projects 1 and 2

This repository contains two dashboard-based data visualization projects. The summaries below are based on the project outputs in `MiniProject1.pdf` and `MiniProject2.pdf`, together with the uploaded raw and cleaned datasets.

## MiniProject1: Planetary Data Dashboard

### Dataset

The exoplanet analysis includes two versions of the data. `Raw.csv` contains **5,986 records and 10 columns**: planet name, planet status, mass, mass uncertainty bounds, minimum mass (`mass_sini`), minimum-mass uncertainty bounds, radius, and radius uncertainty. The raw file contains **28,234 missing cells**, so it is useful for preserving the original observations and status information but requires preprocessing for complete numerical analysis. Every raw record is labeled `Confirmed` in the available `planet_status` field.

`Cleaned_Exoplanet_Data_Final.csv` contains **3,062 records and 8 fully populated columns**: planet name, mass, mass uncertainty bounds, minimum-mass uncertainty bounds, radius, and radius uncertainty. Each cleaned planet name matches a record in the raw file. The cleaned file removes the raw `planet_status` and `mass_sini` columns and provides a complete numerical table for analysis. Because the cleaned mass column contains more populated values than the raw mass column, the cleaning process appears to include value selection or derivation rather than only deleting incomplete rows; the exact transformation should be documented separately if a formal data-preparation log is available.

The dashboard therefore combines the strengths of both files: the raw dataset supports the status-count view, while the cleaned dataset supports the mass, radius, and ranking analyses.

### Visualizations

| Visualization | Dataset role | Purpose |
|---|---|---|
| Number of Planets by Planet Status | Raw dataset | Shows the distribution of planets by status. The available records are dominated by the `Confirmed` category. |
| Top 10 Planets by Mass | Cleaned dataset | Ranks the ten planets with the greatest recorded mass. |
| Relationship Between Planet Mass and Radius | Cleaned dataset | Uses a scatter plot to examine the mass–radius relationship and highlight unusual observations. |

### Key Findings

The raw status field shows a dataset dominated by confirmed planets. The cleaned numerical data reveal a highly skewed mass distribution: a small number of planets are substantially more massive than the majority. The mass–radius scatter plot places most observations in a lower-mass, smaller-radius cluster, while a limited number of extreme observations appear as outliers. These patterns suggest that the dataset contains a large central population together with a small set of unusually large or massive planets.

## MiniProject2: Chocolate Sales Dashboard

### Dataset

The second project uses a chocolate-product sales dataset. The dashboard represents product, sales amount, number of boxes, cost per box, team, and geography or country. These fields support comparisons of product performance, sales volume, team contribution, unit cost, and geographic coverage.

### Visualizations

| Visualization | Purpose |
|---|---|
| Sum of Amount by Product | Compares total sales amount across chocolate products. |
| Sum of Boxes by Product | Compares sales or shipment volume by product. |
| Sum of Boxes by Team | Shows how box volume is distributed among teams. |
| Sum of Cost per Box by Product | Ranks products by cost per box. |
| Geographic Map | Displays the international distribution of sales activity. |
| Team and Geography Filters | Allow the dashboard to be explored by selected team and location. |

### Key Findings

A small group of products contributes disproportionately to both sales amount and box volume. Peanut Butter Cubes appear as a leading product in both measures, followed by other high-volume products such as Milk Bars and Eclairs. Box volume is distributed across several teams, with no single team overwhelmingly controlling the total. Cost per box varies meaningfully by product, creating potential differences in pricing and margins. The map indicates that the sales activity spans multiple countries and regions.

## Overall Takeaway

Together, the projects demonstrate how dashboards can convert raw records into interpretable comparisons. MiniProject1 emphasizes data preparation, distribution, ranking, and outlier detection in exoplanet data, whereas MiniProject2 emphasizes product performance, team contribution, cost comparison, geographic coverage, and interactive filtering.

## Source Files

| File | Description |
|---|---|
| `Raw.csv` | Original exoplanet dataset with status, minimum-mass, uncertainty, and missing-value fields. |
| `Cleaned_Exoplanet_Data_Final.csv` | Cleaned exoplanet analysis table with 3,062 complete records and 8 columns. |
| `MiniProject1.pdf` | Exoplanet dashboard containing the status, mass-ranking, and mass–radius visualizations. |
| `MiniProject2.pdf` | Chocolate sales dashboard containing product, team, cost, geography, and filter visualizations. |
