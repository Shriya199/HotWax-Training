### QUESTION 3 - Average Number of Shipments per Month

Calculate the average number of shipments made per month by dividing the total number of shipments by the number of months.

```sql
SELECT 
    STATUS_ID,
    MIN(CREATED_DATE),
    MAX(CREATED_DATE),
    COUNT(SHIPMENT_ID) / 56 AS Avg_Shipments_Per_Month
FROM 
    shipment s
WHERE 
    STATUS_ID = "SHIPMENT_SHIPPED";
```
### Execution Plan

| Type  | Cost   | Rows   |
|-------|--------|--------|
| Table | 540.41 | 20,452 |
