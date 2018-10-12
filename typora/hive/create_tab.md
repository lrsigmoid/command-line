#Hive建表标准

```sql
use app;
CREATE EXTERNAL TABLE r_sku_to_chnlid_da
(
sku_id      string
,chnl_id    string
,cid3       string
)
PARTITIONED BY (dt string)
ROW FORMAT DELIMITED FIELDS TERMINATED BY '\t'
NULL DEFINED AS ""
STORED AS ORC
LOCATION '/user/recsys/recpro/app.db/r_sku_to_chnlid_da'
```

