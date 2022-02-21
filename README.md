# NYC Taxi Data
Preprocessed NYC Taxi Data (70GB)

## How to Download?
Refer this link

## Benchmark Query
### Query 1
```sql
SELECT cab_type, count(*) FROM fb_trips GROUP BY cab_type
```
### Query 2
```sql
SELECT passenger_count, avg(total_amount) FROM fb_trips GROUP BY passenger_count
```
### Query 3
```sql
SELECT passenger_count, substring(pickup_yyyyMMddhh, 1, 4), count(*) FROM fb_trips 
GROUP BY passenger_count, 
         substring(pickup_yyyyMMddhh, 1, 4)
```
### Query 4
```sql
SELECT passenger_count,
       substring(pickup_yyyyMMddhh, 1, 4),
       round_trip_distance,
       count(*)
FROM fb_trips
GROUP BY 1,
         2,
         3
ORDER BY 2,
         4 desc
```
