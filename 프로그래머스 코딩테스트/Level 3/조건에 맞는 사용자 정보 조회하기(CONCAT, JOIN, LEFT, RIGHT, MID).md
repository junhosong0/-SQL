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
- CONCAT_WS를 써서 더 깔끔하게 코딩, JOIN없이 서브쿼리로 조건문 추가

```sql
SELECT USER_ID, NICKNAME, 
       CONCAT_WS(' ', CITY, STREET_ADDRESS1, 
                            STREET_ADDRESS2) AS 전체주소, 
       CONCAT_WS('-', SUBSTRING(TLNO, 1,3), 
                      SUBSTRING(TLNO, 4,4), 
                      SUBSTRING(TLNO, 8,4)) AS 전화번호
FROM USED_GOODS_USER 
WHERE USER_ID IN ( SELECT WRITER_ID
                   FROM USED_GOODS_BOARD 
                   GROUP BY WRITER_ID
                   HAVING COUNT(*) >= 3)
ORDER BY USER_ID DESC

```
