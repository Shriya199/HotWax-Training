# Q1:  Total number of shipments in January 2022 first quarter

### Description

#### Determine the total count of shipments made during the first quarter of 2022, specifically in the month of January.
---

## SQL Query

```sql
SELECT
    COUNT(CASE 
             WHEN ss.STATUS_DATE >= '2022-01-01 00:00:00' 
                  AND ss.STATUS_DATE < '2022-04-01 00:00:00' THEN ss.SHIPMENT_ID
         END) AS Shipment_in_First_Quarter,
    COUNT(CASE 
             WHEN ss.STATUS_DATE >= '2022-01-01 00:00:00' 
                  AND ss.STATUS_DATE < '2022-02-01 00:00:00' THEN ss.SHIPMENT_ID
         END) AS Shipment_in_January
FROM
    shipment_status ss
WHERE
    ss.status_id = 'SHIPMENT_SHIPPED';

```
## Execution Plan

| **Type**   | **Cost** | **Rows** |
|------------|----------|----------|
| Select     | 6275.95  | 54832    |
