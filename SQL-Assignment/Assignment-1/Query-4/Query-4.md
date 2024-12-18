# Question 4 - Shipped Units By Location

## Objective
Identify the number of units that have been shipped, categorized by different locations; Gain insights into the distribution of shipped units across various locations.

---

## SQL Query

```sql
SELECT
    s.ORIGIN_FACILITY_ID, 
    COUNT(si.quantity) AS shipment_count
FROM
    shipment_item si
JOIN
    shipment s 
ON
    s.SHIPMENT_ID = si.SHIPMENT_ID
WHERE
    s.STATUS_ID = 'shipment_shipped' 
    AND s.DESTINATION_FACILITY_ID IS NULL
GROUP BY
    ORIGIN_FACILITY_ID;
```

## Execution Plan 

| **Type**   | **Cost**  | **Rows** |
|------------|-----------|----------|
| SELECT     | 6585.54   | 19021    |



