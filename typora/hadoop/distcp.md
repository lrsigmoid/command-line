在新集市执行：

```shell
hadoop distcp -m 500 -update -skipcrccheck hdfs://BJYF-Druid-17238.hadoop.jd.local:8020/user/recsys/recpro/app.db/p_sku_to_image_assessment /user/recsys/recpro/app.db/p_sku_to_image_assessment
```



旧集市：hdfs://BJYF-Druid-17238.hadoop.jd.local:8020

新集市：hdfs://BJYF-Druid-17237.hadoop.jd.local:8020