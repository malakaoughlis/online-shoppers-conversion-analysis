# Data Dictionary

## Original Dataset Columns

| Column | Type | Description |
|---|---|---|
| `Administrative` | Integer | Number of administrative pages visited during the session. |
| `Administrative_Duration` | Numeric | Total time spent on administrative pages. |
| `Informational` | Integer | Number of informational pages visited during the session. |
| `Informational_Duration` | Numeric | Total time spent on informational pages. |
| `ProductRelated` | Integer | Number of product-related pages visited during the session. |
| `ProductRelated_Duration` | Numeric | Total time spent on product-related pages. |
| `BounceRates` | Numeric | Average bounce rate of the pages visited during the session. |
| `ExitRates` | Numeric | Average exit rate of the pages visited during the session. |
| `PageValues` | Numeric | Average value of pages visited before an e-commerce transaction. |
| `SpecialDay` | Numeric | Closeness of the visit date to a special shopping day. |
| `Month` | Text | Month in which the session occurred. |
| `OperatingSystems` | Category code | Anonymised operating-system code. |
| `Browser` | Category code | Anonymised browser code. |
| `Region` | Category code | Anonymised geographic-region code. |
| `TrafficType` | Category code | Anonymised traffic-source code. |
| `VisitorType` | Text | Visitor classification: new, returning or other. |
| `Weekend` | Boolean | Indicates whether the session occurred during the weekend. |
| `Revenue` | Boolean | Target variable indicating whether the session ended in a purchase. |

## Cleaned Dataset Changes

The cleaned dataset contains the same 12,330 rows and adds one column:

| Column | Type | Description |
|---|---|---|
| `month_number` | Integer | Numeric month order used to sort months chronologically in Power BI. |

Additional cleaning steps:

- column names converted to lowercase;
- leading and trailing spaces removed from text columns;
- `June` standardised to `Jun`;
- underscores removed from visitor-type labels;
- `weekend` converted from Boolean to `0` and `1`;
- `revenue` converted from Boolean to `0` and `1`;
- no rows removed;
- 125 fully identical rows retained because no unique session identifier is available.

## Power BI-ready Columns

The file `online_shoppers_powerbi_ready.csv` adds:

| Column | Description |
|---|---|
| `purchase_status` | `Achat` or `Pas d'achat`. |
| `period` | `Week-end` or `Semaine`. |
| `product_pages_group` | Product-page count band used in visuals. |
| `product_pages_group_order` | Sorting order for product-page bands. |
| `exit_rate_group` | Exit-rate band used in visuals. |
| `exit_rate_group_order` | Sorting order for exit-rate bands. |
| `traffic_type_label` | Readable label such as `Type 1`, `Type 2`, etc. |
