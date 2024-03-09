![20240309_210923](https://github.com/junhosong0/MySQL/assets/117610783/e4033ae3-f899-4593-ab4b-c002d0ba0d67)

![20240309_210942](https://github.com/junhosong0/MySQL/assets/117610783/14078184-d24c-4552-b4b0-adcc3bd2fd5a)


**내코드**
```sql
select ANIMAL_ID, i.NAME
FROM ANIMAL_INS i
JOIN ANIMAL_OUTS o USING(ANIMAL_ID)
ORDER BY DATEDIFF(o.DATETIME, i.DATETIME) desc
LIMIT 2
```

**배울것**
- ORDER BY 절에는 기존 컬럼만 가능한게 아니라 함수를 사용하여 조건을 써서도 order by를 할 수 있다. 위에 내코드를 하면서 알아냄.
- 
```sql

```
