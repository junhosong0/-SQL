

![20240313_211908_1](https://github.com/junhosong0/MySQL/assets/117610783/61637c77-45ad-4d70-b3c7-86558da022a1)

![20240313_211908_2](https://github.com/junhosong0/MySQL/assets/117610783/26a5655c-e5cb-4a17-a7e3-6707e5151f23)


**내코드**
- 서브 쿼리를 사용할때 서브쿼리에서 뽑아낸 값들이 2행 이상인 경우 where 절에 = 를 사용하면 에러가 뜬다. 이때 where in을 사용하면 원하는 조건을 비교해서 가져올 수 있

```sql
select id, name, host_id
from places
where host_id in (SELECT host_id
from places
group by host_id
having count(host_id) >= 2)
order by id;
```




**배울것**
- with 절을 통해 헤비 유저에 대한 데이터를 뽑고 기존 테이블에서 쉽게 조회할 수 있게 함.

```sql
with temp as (
SELECT host_id, count(*) cnt from places
group by host_id having cnt >=2
)

select * from places 
where host_id in (select host_id from temp)
order by 1

```
