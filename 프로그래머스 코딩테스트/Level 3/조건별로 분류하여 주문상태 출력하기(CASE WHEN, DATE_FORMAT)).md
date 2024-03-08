
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
- JOIN USING을 써서 푼 것

```sql
SELECT ANIMAL_ID, I.NAME
FROM ANIMAL_INS I JOIN ANIMAL_OUTS O USING(ANIMALID)
WHERE I.DATETIME > O.DATETIME
ORDER BY I.DATETIME ASC
```
