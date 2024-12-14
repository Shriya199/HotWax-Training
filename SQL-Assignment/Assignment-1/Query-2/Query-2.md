# Question 2: Shipment by Tracking Number

### Description

#### View or analyze shipments based on their unique tracking numbers. Each shipment is identified and tracked using a specific tracking number.
---

## SQL Query

```sql
SELECT
    SHIPMENT_ID,
    TRACKING_ID_NUMBER
FROM
    shipment_route_segment srs
WHERE
    srs.TRACKING_ID_NUMBER IS NOT NULL;
```
## Execution Plan

| **Type**   | **Cost** | **Rows** |
|------------|----------|----------|
| Select     | 4625.83  | 41080    |
