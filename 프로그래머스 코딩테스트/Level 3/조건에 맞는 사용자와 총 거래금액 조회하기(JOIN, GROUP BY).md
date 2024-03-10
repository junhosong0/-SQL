
![20240310_154438](https://github.com/junhosong0/MySQL/assets/117610783/64f094aa-02c2-4b25-abf1-a3fdba539699)


![20240310_154455](https://github.com/junhosong0/MySQL/assets/117610783/d4e718e4-7f07-4001-baf1-6ee951ef1186)




**내코드**
```sql
SELECT b.writer_id, u.nickname, sum(price) as "총거래금액"
from used_goods_board b
join used_goods_user u 
on b.writer_id = u.user_id
where status = "DONE"
group by writer_id
having sum(price) >= 700000
order by sum(price) asc
```


**배울것**
- 문제를 제대로 세세하게 안봐서 틀리는 경우가 있음. 위에서 "완료된 거래" 부분을 놓쳐서 계속 틀렸음.
- 아래와 같이 ALIAS 안써도 되고 JOIN USING()으로 해도 됨

```sql
SELECT WRITER_ID, NICKNAME, SUM(PRICE) AS TOTAL_SALES
FROM USED_GOODS_BOARD JOIN USED_GOODS_USER ON WRITER_ID = USER_ID 
WHERE STATUS = 'DONE'
GROUP BY WRITER_ID
HAVING SUM(PRICE) >= 700000
ORDER BY TOTAL_SALES ASC
```

- JOIN을 안써도 됨. GROUP BY만으로 가능

```sql
SELECT a.user_id, a.nickname, sum(b.price) as total_sales
from used_goods_user a, used_goods_board b
where a.user_id=b.writer_id and status='DONE'
group by b.writer_id
having sum(b.price)>=700000
order by total_sales
```
