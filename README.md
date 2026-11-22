# Video Game Sales Analysis | Excel & Tableau

**By Shaquille Thomas**

An analysis of 542 video game records using Excel PivotTables, charts, and an interactive Tableau dashboard. This walkthrough follows the project from the original dataset through preparation, analysis, visualization, and interpretation.

## Project Objective

Explore four questions within the supplied dataset:

- Which genres have the highest recorded global sales?
- Which platforms account for the most recorded game sales?
- How do recorded sales compare across regions?
- How do recorded sales differ by game release year?

The findings describe the included records and do not represent the entire video game industry.

## Tools Used

- **Microsoft Excel:** data review, preparation, PivotTables, and charts.
- **Tableau Public Desktop:** worksheets, dashboard development, and interactive filtering.

## 1. Original Dataset

The original Excel file contains **546 records**, with fields for rank, game name, platform, release year, genre, publisher, regional sales, and global sales.

The original file is preserved separately from the analysis workbook so readers can compare the starting data with the prepared version.

[View the original dataset](<vgsales_1 (original dataset).xlsx>)

![Original Excel dataset](<Walkthrough Screenshots/original dataset.png>)

**Source limitation:** The original source and sales unit scale have not been independently verified. Sales figures are therefore described as reported values, without assuming currency or millions of units.

## 2. Data Preparation

I reviewed the release-year field and identified **four records with missing years**, shown as `N/A`.

![Records with missing release years](<Walkthrough Screenshots/missing release years.png>)

These records were excluded from the analysis dataset, leaving **542 records** with known release years. The original dataset remains available separately.

| Preparation stage | Records |
|---|---:|
| Original dataset | 546 |
| Excluded records with missing release years | 4 |
| Prepared analysis dataset | 542 |

![Prepared dataset](<Walkthrough Screenshots/cleaned dataset.png>)

Excluding missing years allows consistent comparisons across release-year groups. It does not establish that the remaining data is complete or error-free.

## 3. Excel Analysis

Using the prepared data, I created PivotTables to summarize recorded sales across four dimensions.

| Analysis | Grouping | Aggregation |
|---|---|---|
| Release-year comparison | Year | Sum of Global Sales |
| Regional comparison | North America, Europe, Japan, Other | Sum of each regional sales field |
| Platform comparison | Platform | Sum of Global Sales |
| Genre comparison | Genre | Sum of Global Sales |

I then created charts from these summaries to compare categories and examine release-year patterns.

![Excel PivotTable analysis](<Walkthrough Screenshots/pivot analysis.png>)

[Download the Excel analysis workbook](<Video Game Sales.xlsx>)

## 4. Tableau Worksheet Development

I connected Tableau to the Excel data and developed four worksheets using the prepared analysis scope.

### Recorded Global Sales by Genre

- Placed **Genre** on Rows.
- Placed **SUM(Global Sales)** on Columns.
- Used horizontal bars sorted by descending sales.
- Displayed sales labels for comparison.

Action has the highest combined recorded global sales, followed by Shooter and Platform.

![Tableau recorded global sales by genre](<Walkthrough Screenshots/tableau global sales by genre.png>)

### Recorded Global Sales by Release Year

- Placed **Year** on Columns.
- Placed **SUM(Global Sales)** on Rows.
- Used a line chart to compare release-year groups.
- Labeled the horizontal axis **Release Year**.

Games released in 2009 have the highest combined recorded sales in the supplied dataset.

**Interpretation:** These values are sales associated with games released in each year. They are not sales transactions occurring during that calendar year.

![Tableau recorded global sales by release year](<Walkthrough Screenshots/tableau global sales by year.png>)

### Regional Sales Comparison

I compared the summed sales fields for North America, Europe, Japan, and Other Regions.

North America has the largest recorded regional total, followed by Europe, Japan, and Other Regions.

![Tableau regional sales comparison](<Walkthrough Screenshots/tableau regional sales comparison.png>)

### Top Platforms by Global Sales

I grouped recorded global game sales by platform and compared the highest totals.

Wii leads within the supplied dataset, followed by Xbox 360 and PlayStation 2. These figures describe **game sales by platform**, rather than console hardware sales.

## 5. Interactive Dashboard

I combined the four worksheets into a single dashboard covering genres, release years, regions, and platforms.

![Complete Tableau dashboard](<Walkthrough Screenshots/complete dashboard.png>)

The dashboard includes a **Genre filter** that updates all four charts, allowing users to explore the same selected category across each view.

### Example: Action Genre

Selecting **Action** updates the dashboard to show the regional, platform, and release-year results for Action games.

![Dashboard filtered to Action games](<Walkthrough Screenshots/action filtered dashboard.png>)

To explore another genre, change the filter selection. Select **All** to return to the complete analysis scope.

## 6. Validation

The main reconciliation points for comparing the Excel and Tableau outputs are:

| Check | Expected result |
|---|---|
| Prepared record count | 542 records |
| Combined recorded global sales | 3,290.81 |
| Leading genre | Action |
| Leading platform | Wii |
| Leading regional sales field | North America |
| Release year with highest combined recorded sales | 2009 |

Compare both tools using the same record scope and filter selections. Tableau may display rounded totals, so use two decimal places when comparing the global sales total.

For dashboard interaction, select **Action** and check that all four charts respond, then return the filter to **All**.

## 7. Key Findings

Within the supplied dataset:

- **Action** has the highest combined recorded global sales, followed by Shooter and Platform.
- **Wii** has the highest recorded game sales by platform, followed by Xbox 360 and PlayStation 2.
- **North America** contributes the largest regional sales total.
- Games released in **2009** account for the highest combined recorded global sales.

These findings describe the dataset's coverage and should not be generalized to the whole market.

## 8. Limitations

- The dataset contains a limited selection of video game records.
- The original source and sales unit scale have not been independently verified.
- Four records with missing release years were excluded from every analysis.
- Release year identifies when a game was released, not when its sales occurred.
- Lower totals for later release years do not establish an overall decline in the gaming industry.
- Platform totals represent recorded game sales, not hardware sales.
- Data preparation and agreement between tools do not independently verify the underlying sales figures.

## 9. How to Explore the Project

| File or folder | Purpose |
|---|---|
| [Original dataset](<vgsales_1 (original dataset).xlsx>) | Inspect the supplied data before preparation |
| [Excel analysis](<Video Game Sales.xlsx>) | Review the prepared data, PivotTables, and charts |
| [Tableau workbook](<Video Game Sales Analysis.twbx>) | Open the worksheets and interactive dashboard |
| [PDF report](<Excel and Tableau Game Sales Analysis.pdf>) | Read the written analysis |
| [Walkthrough screenshots](<Walkthrough Screenshots/>) | Follow the preparation and visualization steps |

### Opening the Files

1. Download the Excel files and open them in Microsoft Excel.
2. Compare the original dataset with the prepared analysis workbook.
3. Review the PivotTables and charts.
4. Download the `.twbx` file and open it in Tableau Public Desktop or Tableau Desktop.
5. Open the dashboard and change the Genre filter.
6. Read the PDF report for the findings and limitations.

## Skills Demonstrated

Data preparation, missing-value handling, Excel PivotTables, aggregation, chart development, Tableau worksheets, interactive dashboard design, comparison across tools, and analytical documentation.
