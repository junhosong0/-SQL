![20240311_193211](https://github.com/junhosong0/MySQL/assets/117610783/b84c01db-c3e3-451f-87a9-fbae81989d11)

![20240311_193231](https://github.com/junhosong0/MySQL/assets/117610783/81322312-53c5-468e-b917-4fa3f2f0bbc4)


**내코드**
- left join은 먼저 지정한 테이블 조건의 모든 내역을 기준으로 이후에 지정한 테이블을 붙여준다. 만약 먼저 지정한 테이블 조건에는 있는 내용이 이후에 지정한 테이블 조건에 없으면 null값으로 들어간다.
- 이 경우 입양을 보낸 동물들 중 보호소에 보호된 내용이 유실된 경우를 추출해야 하기 때문에 입양보낸 animal_outs 테이블을 기준으로 animal_ins테이블을 오른쪽에 붙여준다.

```sql
SELECT o.animal_id, o.name
FROM animal_outs o
left join animal_ins i on i.animal_id = o.animal_id
where i.animal_id is null
order by o.animal_id
```


**배울것**
- left join도 using으로 간편화 할 수 있음
- animal_ins에만 없는 데이터들을 추출하면 되기 때문에 animal_ins에만 있는 컬럼이름 중 아무거나 where절에서 is null로 조회하면 됨. 


```sql
SELECT ANIMAL_ID, O.NAME
FROM ANIMAL_OUTS O LEFT JOIN ANIMAL_INS USING(ANIMAL_ID) 
WHERE INTAKE_CONDITION IS NULL
ORDER BY ANIMAL_ID, NAME
```
