## Status

**Dashboard insights aligned to the five defined business questions.**
The insights below are based on the KPI cards, monthly trend, model cards, country table, regional visual, and channel quantity visual shown in the dashboard, with the transaction-level `FactTable` and supporting dimensions from the data model taken into consideration.

---

## Required Evidence-Based Format

### Insight 1: Revenue Trends

**Revenue demonstrates strong and sustained year-over-year growth.**

* Current Revenue: **$1.13B**
* Revenue PY: **$904M**
* Revenue Variance: **+24.7%**
* Approximate revenue increase: **$226M**

**Evidence:** The Revenue KPI shows $1.13B compared with $904M in the prior-year period. The monthly Revenue vs Revenue PY visual also shows current-period revenue above the prior-year comparison across the displayed months.

**Key Insight:**

> **Revenue increased by 24.7% year-over-year, with the monthly trend indicating that the positive performance is sustained across the reporting period rather than being driven by a single month.**

---

### Insight 2: Top Selling Models

**The dashboard shows relatively strong and closely distributed sales among the leading displayed models.**

| Model        | Quantity Sold |
| ------------ | ------------: |
| **BMW Z4**   |       **666** |
| BMW 8 Series |           641 |
| BMW M4       |           620 |
| BMW i8       |           615 |

**Evidence:** The model cards display BMW Z4 with 666 units, followed by BMW 8 Series with 641, BMW M4 with 620, and BMW i8 with 615.

**Key Insight:**

> **BMW Z4 is the leading displayed model with 666 units sold, followed by the BMW 8 Series, M4, and i8. The relatively small gap between these models suggests that sales are distributed across multiple models rather than being heavily concentrated in one model.**

---

### Insight 3: Sales Performance by Country

**Sales performance is strong across several individual countries.**

| Country       | Quantity Sold |     Revenue |
| ------------- | ------------: | ----------: |
| **Argentina** |           621 | **$47.43M** |
| **Colombia**  |       **632** |     $46.95M |
| **Spain**     |           615 |     $45.99M |

**Evidence:** The Sales by Country table shows these countries among the leading displayed markets by both quantity and revenue. The Revenue by Region visual also shows Africa as the leading displayed region.

**Key Insight:**

> **Argentina, Colombia, and Spain are among the strongest individual markets, each generating approximately $46M–$47M in revenue and more than 600 units sold. Colombia leads the displayed countries by quantity, while Argentina leads them by revenue.**

---

### Insight 4: Sales Channel Performance

**Sales volume is distributed unevenly across the sales channels.**

The channel visual shows approximately:

* **Whosales at 7K units** — ~44%
* **Dealership at 5K units** — ~33%
* **Online at 3K units** — ~22%
* **Total: ~15K units**

**Evidence:** The `Qty Sold by Channel` donut chart shows three channel contributions of approximately 7K, 5K, and 3K units.

**Key Insight:**

> **Sales volume is concentrated in the wholesales channel, which accounts for approximately 7K of the 15K units sold, or about 44% of total volume. The remaining channels contribute approximately 5K and 3K units respectively.**

---

### Insight 5: Quantity Sold

**The business recorded approximately 15K units sold across the reporting period.**

**Evidence:** From `Qty Sold by Channel` visual displays approximately **15K total units**, while the individual model and country visuals show substantial sales volumes across multiple products and markets.

**Key Insight:**

> **Approximately 15,000 vehicles were sold during the reporting period, with sales volume distributed across multiple models, countries, and channels. This provides a strong volume base supporting the $1.13B revenue generated.**

---

## Baseline Data Checks

1. **Fact table grain:**
   The `FactTable` represents **individual sales transactions**, making it appropriate for aggregating `Quantity Sold` and `Revenue`.

2. **Date analysis:**
   `Dim_Date` is connected to `FactTable` through `Date`, enabling the monthly Revenue and Revenue PY analysis.

3. **Model analysis:**
   `DimModel` provides the model attributes used to analyse vehicle-level sales and contains the `Car_img` attribute enriched from the separate car-image source file.

4. **Country analysis:**
   `DimCountry` provides `Country` and `Region` attributes for geographic analysis and contains the `C_Flag` attribute enriched from the separate country-image source file.

5. **Channel analysis:**
   `DimChannel` provides the channel attributes used to break down sales volume by channel.

6. **Source files:**
   The analysis originated from three CSV sources: **Sales**, **Car Image URL**, and **Country Image URL**. The image sources were merged into the relevant dimensions during Power Query preparation.

7. **KPI validation:**
   The dashboard reports **$1.13B Revenue, $904M Revenue PY, +24.7% Revenue Variance, and approximately 15K units sold**. These should remain tied to the underlying DAX measures and transaction-level `FactTable` when the dashboard is refreshed.

### Overall dashboard story

> **The business generated $1.13B in revenue, representing 24.7% YoY growth, supported by approximately 15K vehicles sold across multiple models, countries, and sales channels. Performance is relatively diversified across the leading models and geographic markets, while sales volume is more concentrated in the leading channel.**
