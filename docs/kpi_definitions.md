# KPI and Measure Definitions

|Measure|Definition|Interpretation|
|-|-|-|
|`Qty Sold`|`SUM(FactTable\[Quantity Sold])`|Total units in the current filter context|
|`Qty Sold PY`|Recalculates `Qty Sold` one year earlier using `DATEADD`|Prior-year units for comparison|
|`Qty Sold Varience`|`\[Qty Sold] - \[Qty Sold PY]`|Absolute year-over-year change in units|
|`Qty Sold Growth`|`\[Qty Sold Varience] / \[Qty Sold PY]` using `DIVIDE`|Proportional year-over-year unit change|
|`Qty Sold Variance %`|Recalculates the proportional change and returns formatted text with a direction symbol|Display measure rather than a numeric KPI|
|`Qty-Sold\_Spakline`|Generates an SVG polyline and shaded area over selected `Dim\_Date\[MonthNum]` values|Compact unit-sales trend image|
|`Revenue`|`SUM(FactTable\[Revenue])`|Total recorded revenue in the current filter context|
|`Revenue PY`|Recalculates `Revenue` with `SAMEPERIODLASTYEAR`|Prior-year revenue for comparison|
|`Revenue Variance %`|Calculates proportional year-over-year revenue change and returns formatted text with a direction symbol|Display measure rather than a numeric KPI|
|`Revenue\_Spakline`|Generates an SVG polyline and shaded area over selected `Dim\_Date\[MonthNum]` values|Compact revenue trend image|