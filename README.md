# BMW Global Sales Performance Dashboard

## Project Overview

This portfolio project presents a Power BI analysis of BMW vehicle sales across models, countries, regions, channels, and time. The supplied sales file contains 5,000 populated records covering 1 January 2019 through 31 December 2023, plus 778 fully blank rows that require exclusion during data preparation.

The report focuses on revenue and quantity sold, including prior-year comparisons, variances, and compact trend visualizations. The original Power BI report and source files are preserved in the project root.

> Dashboard screenshot: `[NEEDS INPUT]`. Add an exported overview image as `images/dashboard/dashboard-overview.png`, then embed it here.

## Business Problem

Sales stakeholders need a consolidated view of BMW sales performance that supports comparison across time, vehicle models, geography, and sales channels. The exact stakeholder, organizational context, and decision process are `[NEEDS INPUT]`.

See [Business Problem](docs/business_problem.md) and [Objectives](docs/objectives.md).

## Dataset

The main dataset is `BMW_Sales_Data.csv`.

| Attribute | Verified value |
|---|---:|
| Physical rows | 5,778 |
| Populated rows | 5,000 |
| Fully blank rows | 778 |
| Columns | 8 |
| Date range | 2019-01-01 to 2023-12-31 |
| BMW models | 26 |
| Sales countries | 24 |
| Sales regions | 5 |
| Sales channels | 3 |
| Recorded revenue | 376,065,225 |
| Recorded quantity sold | 15,002 |

The currency represented by `Revenue` is `[NEEDS INPUT]`. The data source and whether the records are real, synthetic, or modified are also `[NEEDS INPUT]`.

Supporting files provide model-image URLs, country flag URLs, dashboard assets, and a text record of the applied DAX measures. See [Source and Attribution](docs/source_and_attribution.md).

## Tools and Skills Demonstrated

- Power BI dashboard development
- Power Query data preparation `[NEEDS INPUT: confirm transformations performed]`
- DAX measures and time intelligence
- Data modelling with a fact table and date dimension
- KPI definition and year-over-year comparison
- Geographic, product, channel, and time-based analysis
- SVG sparklines generated with DAX

## Analytical Workflow

1. Load the sales and supporting lookup files.
2. Exclude fully blank sales rows and assign appropriate data types.
3. Build or use the `FactTable` and `Dim_Date` model objects referenced by the supplied DAX.
4. Relate model and geographic lookup data as implemented in the Power BI file.
5. Calculate revenue, quantity sold, prior-year values, variance, growth, and trend measures.
6. Build interactive report views for business performance analysis.
7. Validate totals and filter behavior. `[NEEDS INPUT: confirm validation procedure]`

See [Methodology](docs/methodology.md), [Data Model](docs/data_model.md), and [KPI Definitions](docs/kpi_definitions.md).

## Dashboard Features

The source files verify measures for revenue, quantity sold, previous-year comparison, variance indicators, and DAX-generated sparklines. The exact report pages, slicers, visual interactions, drill-through behavior, and tooltip configuration are `[NEEDS INPUT]` because they cannot be established reliably from the binary `.pbix` alone in this environment.

See [Dashboard Guide](docs/dashboard_guide.md).

## Key Insights

Verified business findings have not yet been supplied or exported from the report. No ranking, trend, or performance conclusion is asserted in this portfolio until it is validated against the dashboard.

See [Key Insights](docs/key_insights.md) for the required evidence-based format.

## Repository Structure

```text
BMW_Sales_Data/
|-- README.md
|-- LICENSE.md
|-- .gitignore
|-- BMW_Sales_Dashboard.pbix
|-- BMW_Sales_Data.csv
|-- Applied Measures.txt
|-- BMW_Image_URLs.csv
|-- Car Imagess.csv
|-- Countries with Flags URL.csv
|-- icon/
|-- docs/
|   |-- business_problem.md
|   |-- objectives.md
|   |-- methodology.md
|   |-- data_dictionary.md
|   |-- kpi_definitions.md
|   |-- data_model.md
|   |-- key_insights.md
|   |-- dashboard_guide.md
|   `-- source_and_attribution.md
`-- images/
    |-- dashboard/
    `-- data-model/
```

## How to Use

1. Install Power BI Desktop `[NEEDS INPUT: minimum tested version]`.
2. Open `BMW_Sales_Dashboard.pbix`.
3. If Power BI reports missing sources, update the data-source paths to the CSV files in this project root.
4. Refresh the model and compare the resulting totals with the documented dataset profile.

## Limitations

- The main CSV includes 778 fully blank rows.
- Revenue currency is not documented.
- Data provenance and usage rights are not documented.
- External image and flag URLs may change or become unavailable.
- `BMW_Image_URLs.csv` contains placeholder GitHub URLs using `<your-user>`.
- The lookup file `Car Imagess.csv` and several DAX measure names contain spelling errors; they are documented as implemented to avoid misrepresenting the report.
- The text export of variance measures contains corrupted direction symbols, likely due to character encoding.
- Cost, profit, margin, customer, target, and inventory fields are not present in the supplied sales dataset.

## Author

- Name: `[NEEDS INPUT]`
- Role: Data Analyst
- Portfolio: `[NEEDS INPUT]`
- LinkedIn: `[NEEDS INPUT]`
- Contact: `[NEEDS INPUT]`

## License

`[NEEDS INPUT]` See [LICENSE.md](LICENSE.md).
