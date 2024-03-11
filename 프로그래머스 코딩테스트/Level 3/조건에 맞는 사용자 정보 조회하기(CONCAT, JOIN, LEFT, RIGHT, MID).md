![20240311_194202](https://github.com/junhosong0/MySQL/assets/117610783/8394162f-374d-4b82-a7a0-b138f82a6377)

![20240311_194218](https://github.com/junhosong0/MySQL/assets/117610783/211d3faa-bc4c-42c4-ad5f-c181b9f917d9)



**내코드**
- CONCAT으로 서로 다른 컬럼들의 값을 합치거나 문자열을 추가하여 추출할 수 있다

```sql
SELECT user_id, nickname, CONCAT(city, ' ', street_address1, ' ', street_address2) as 전체주소, concat(left(tlno,3), '-', mid(tlno,4,4), '-', right(tlno,4)) as tlno
from used_goods_user u
join used_goods_board b on u.user_id = b.writer_id 
group by writer_id
having count(writer_id) >= 3
order by u.user_id desc
```




**배울것**
-

```sql

```
