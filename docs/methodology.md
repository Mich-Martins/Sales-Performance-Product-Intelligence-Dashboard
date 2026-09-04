# Methodology

## 1. Source Inspection

The project contains a main sales CSV, two BMW image lookups, a country flag lookup, local image assets, a DAX measures text file, and a Power BI report.

## 2. Data Profiling

The following properties were verified directly from `BMW_Sales_Data.csv`:

| Check | Result |
|---|---:|
| Physical records | 5,778 |
| Populated records | 5,000 |
| Fully blank records | 778 |
| Valid populated date range | 2019-01-01 to 2023-12-31 |
| Populated models | 26 |
| Populated countries | 24 |
| Populated regions | 5 |
| Populated channels | 3 |

## 3. Data Cleaning

The source profile indicates that fully blank records should be excluded. The exact Power Query steps implemented in the `.pbix`, including type changes, renaming, error handling, or query dependencies, are `[NEEDS INPUT: export or describe Power Query transformations]`.

Recommended validation rules, without claiming they are already implemented:

- Remove rows where all sales fields are blank.
- Parse `Date` explicitly as `dd/MM/yyyy`.
- Store `Year`, `Revenue`, and `Quantity Sold` as numeric fields.
- Confirm that revenue and quantity values are non-negative.
- Standardize model, region, country, and channel labels.
- Check lookup keys for uniqueness before relationships are created.

## 4. Data Modelling

The DAX source explicitly references `FactTable` and `Dim_Date`. This confirms the presence or intended use of a sales fact table and a date dimension. Other model tables, relationship directions, cardinalities, calculated columns, and hidden fields are `[NEEDS INPUT]`.

## 5. Measure Development

Ten measures are recorded in `Applied Measures.txt`. They calculate revenue, quantity sold, prior-year comparisons, variances or growth, formatted directional indicators, and SVG sparklines. See `kpi_definitions.md`.

## 6. Visualization

The report file is `BMW_Sales_Dashboard.pbix`. A verified inventory of pages, visuals, filters, tooltips, bookmarks, and interactions is `[NEEDS INPUT]`.

## 7. Validation

The raw populated rows sum to:

- Revenue: 376,065,225
- Quantity sold: 15,002

These figures are source-data checks, not assertions about the dashboard's current filter context. Dashboard reconciliation results are `[NEEDS INPUT]`.
