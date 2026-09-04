# Data Model

## Verified Model Components
The original project source consisted of three CSV files: the sales transaction file, a car image URL file, and a country flag/image URL file. During data preparation, the image URL datasets were merged into the corresponding model and country dimensions. As a result, DimModel contains the Car_img attribute and DimCountry contains the C_Flag attribute. The original image lookup tables may remain in the Power BI model as supporting/source tables but are not required as active relationship paths when the image attributes have already been incorporated into the dimensions.

| Relationship             | Key         | Status        | Explanation                                                |
| ------------------------ | ----------- | ------------- | ---------------------------------------------------------- |
| `Dim_Date → FactTable`   | `Date`      | **Confirmed** | One-to-many relationship supporting date-based analysis    |
| `DimModel → FactTable`   | `ModelID`   | **Confirmed** | Dimension filters transaction-level sales by vehicle model |
| `DimCountry → FactTable` | `CountryID` | **Confirmed** | Dimension filters transaction-level sales by country       |
| `DimChannel → FactTable` | `ChannelID` | **Confirmed** | Dimension filters transaction-level sales by sales channel |

| Source/Supporting Data | Transformation                           | Current Role                  |
| ---------------------- | ---------------------------------------- | ----------------------------- |
| Car Image URL CSV      | Merged into `DimModel` using `Model`     | Provides `DimModel[Car_img]`  |
| Country Image URL CSV  | Merged into `DimCountry` using `Country` | Provides `DimCountry[C_Flag]` |

## Relationships and Merge Concept
There are actually two different concepts here:

### Relationships
These are the connections between your model tables:

Dim_Date ──────► FactTable
Dim_Model ─────► FactTable
Dim_Country ───► FactTable
Dim_Channel ───► FactTable

### Merges
These happened during Power Query/data preparation:

Car Image CSV
      │
      │ Merge on Model
      ▼
  DimModel


Country Flag CSV
      │
      │ Merge on Country
      ▼
  DimCountry

A Power Query merge is not the same thing as a Power BI model relationship.

Model screenshot: `images/data-model/data-model.png`.
