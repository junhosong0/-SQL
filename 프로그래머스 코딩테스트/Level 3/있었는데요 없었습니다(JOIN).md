![image](https://github.com/junhosong0/MySQL/assets/117610783/3072cea3-1383-45ea-b76b-bace88503b57)

![20240308_164844](https://github.com/junhosong0/MySQL/assets/117610783/89506710-fba4-4ec0-b08d-0d2c7f309eae)



**내코드**
```sql
SELECT i.animal_id, i.name
from animal_ins i
left join animal_outs o
on i.animal_id = o.animal_id
where i.datetime > o.datetime
order by i.datetime
```



**배운 것**
- 중첩 if문을 사용해서 풀 수 있음.

```sql
SELECT ORDER_ID,PRODUCT_ID,date_format(OUT_DATE,'%Y-%m-%d') as OUT_DATE, 
    if(out_date <= '2022-05-01','출고완료',if(out_date is null,'출고미정','출고대기')) as '출고여부'
from food_order
order by order_id;
```
