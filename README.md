# FLO Müşteri Segmentasyonu
Data Set: Private by FLO

# SQL KOD
SELECT TOP 10 * FROM flo_data_20k$
 
SELECT master_id,order_channel,last_order_channel,first_order_date,last_order_date,
last_order_date_online,last_order_date_offline,interested_in_categories_12,
CONVERT (FLOAT , REPLACE(order_num_total_ever_online ,',','.')) AS ORDER_NUM_EVER_ONLINE ,
CONVERT (FLOAT ,REPLACE(order_num_total_ever_offline ,',','.')) AS ORDER_NUM_EVER_OFFLINE,
CONVERT (FLOAT ,REPLACE(customer_value_total_ever_offline ,',','.')) AS CUSTOMER_VALUE_OFFLINE,
CONVERT (FLOAT ,REPLACE(customer_value_total_ever_online ,',','.')) AS CUSTOMER_VALUE_ONLINE
INTO ##C
FROM flo_data_20k$

SELECT * INTO FLO FROM ##C

![image](https://user-images.githubusercontent.com/92053918/195984313-ec370d3a-3fbc-440e-b7cc-b4d978d5513e.png)
