# Data Dictionary

## Main Sales Data

Source: `BMW\_Sales\_Data.csv`

|Field|Observed role|Example|Notes|
|-|-|-|-|
|`Date`|Transaction date|`01/01/2019`|Text source format appears to be `dd/MM/yyyy`; 778 blank rows|
|`Year`|Calendar year|`2019`|Values span 2019-2023 in populated rows|
|`Model`|BMW model|`BMW X2`|26 distinct populated values|
|`Revenue`|Recorded sales revenue|`94654`|Currency and tax treatment are `Price`|
|`Quantity Sold`|Units sold|`2`|Aggregated by the `Qty Sold` measure|
|`Region`|Sales region|`Africa`|Africa, Asia, Europe, North America, South America|
|`Country`|Sales country|`Nigeria`|24 distinct populated values|
|`Channel`|Sales channel|`Wholesale`|Dealership, Online, Wholesale|

The grain of the dataset is transaction-level. Each populated row represents a single sales transaction associated with a specific date, model, country, and sales channel.


## Car Image Lookup

Source: `Car Imagess.csv`

|Field|Observed role|Notes|
|-|-|-|
|`Model`|Model lookup key|26 rows|
|`img`|External model image URL|Third-party availability and reuse rights are valid|

## Country Flag Lookup

Source: `Countries with Flags URL.csv`

|Field|Observed role|Notes|
|-|-|-|
|`Country`|Country name|251 rows|
|`Country code`|Two-letter code|Observed lowercase values|
|`Region`|Lookup region grouping|Uses values such as `EMEA`; not the same classification as the sales table|
|`Flag`|External flag image URL|Third-party availability and reuse rights are valid|

## Model Objects Referenced by DAX

|Object|Evidence|Description|
|-|-|-|
|`FactTable`|`Applied Measures.txt`|Contains at least `Revenue` and `Quantity Sold`|
|`Dim\_Date`|`Applied Measures.txt`|Contains at least `Date` and `MonthNum`|

Additional model columns and calculated objects are available.

