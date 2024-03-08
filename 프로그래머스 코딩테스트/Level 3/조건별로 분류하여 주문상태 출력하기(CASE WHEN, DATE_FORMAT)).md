
![20240307_195044_1](https://github.com/junhosong0/MySQL/assets/117610783/d1ef58c7-4b7f-4bd5-9759-363b96cef52f)

![20240307_195044_2](https://github.com/junhosong0/MySQL/assets/117610783/1cdd89d5-27c5-416a-a126-05367774f6c0)


**내코드**
```sql
SELECT order_id, product_id, date_format(out_date, '%Y-%m-%d') as out_date,
case 
    when out_date <= '2022-05-01' then '출고완료' 
    when out_date > '2022-05-01' then '출고대기' 
    when out_date is null then '출고미정' 
end as '출고여부'
from food_order
order by order_id;
```



**배운 것**
- 중첩 if문을 사용해서 풀 수 있음.

```sql
SELECT ORDER_ID,PRODUCT_ID,date_format(OUT_DATE,'%Y-%m-%d') as OUT_DATE, 
    if(out_date <= '2022-05-01','출고완료',if(out_date is null,'출고미정','출고대기')) as '출고여부'
from food_order
order by order_id;
```
