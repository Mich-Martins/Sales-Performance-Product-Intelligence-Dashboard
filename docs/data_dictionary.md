# Data Dictionary

## Main Sales Data

Source: `BMW\_Sales\_Data.csv`

|Field|Observed role|Example|Notes|
|-|-|-|-|
|`Date`|Transaction date|`01/01/2019`|Text source format appears to be `dd/MM/yyyy`; 778 blank rows|
|`Year`|Calendar year|`2019`|Values span 2019-2023 in populated rows|
|`Model`|BMW model|`BMW X2`|26 distinct populated values|
|`Revenue`|Recorded sales revenue|`94654`|Currency and tax treatment are `\[NEEDS INPUT]`|
|`Quantity Sold`|Units sold|`2`|Aggregated by the `Qty Sold` measure|
|`Region`|Sales region|`Africa`|Africa, Asia, Europe, North America, South America|
|`Country`|Sales country|`Nigeria`|24 distinct populated values|
|`Channel`|Sales channel|`Wholesale`|Dealership, Online, Wholesale|

The grain of a populated row appears to be a dated model-country-channel sales observation. Whether each row represents an individual transaction or an aggregated observation is `\[NEEDS INPUT]`.

## BMW Image Lookup

Source: `BMW\_Image\_URLs.csv`

|Field|Observed role|Notes|
|-|-|-|
|`BMW Model`|Model lookup key|26 rows|
|`img\_URL`|Model image URL|URLs use the unresolved placeholder `<your-user>`|

## Car Image Lookup

Source: `Car Imagess.csv`

|Field|Observed role|Notes|
|-|-|-|
|`Model`|Model lookup key|26 rows|
|`img`|External model image URL|Third-party availability and reuse rights are `\[NEEDS INPUT]`|

## Country Flag Lookup

Source: `Countries with Flags URL.csv`

|Field|Observed role|Notes|
|-|-|-|
|`Country`|Country name|251 rows|
|`Country code`|Two-letter code|Observed lowercase values|
|`Region`|Lookup region grouping|Uses values such as `EMEA`; not the same classification as the sales table|
|`Flag`|External flag image URL|Third-party availability and reuse rights are `\[NEEDS INPUT]`|

## Model Objects Referenced by DAX

|Object|Evidence|Description|
|-|-|-|
|`FactTable`|`Applied Measures.txt`|Contains at least `Revenue` and `Quantity Sold`|
|`Dim\_Date`|`Applied Measures.txt`|Contains at least `Date` and `MonthNum`|

Additional model columns and calculated objects are `\[NEEDS INPUT]`.

