
![20240312_172850](https://github.com/junhosong0/MySQL/assets/117610783/c6db8391-fd3e-4aa2-b1c3-b646e1cc0cac)

![20240312_172831](https://github.com/junhosong0/MySQL/assets/117610783/92b20749-8516-4989-9a96-908e4ee1081d)




**내코드**
- 내가 직접 정답 코드를 작성하지 못해 다른 사람의 정답을 보고 배웠다....

```sql

```




**배울것**
- history_id는 PK개념으로 중복허용 없음
- car_id는 중복이 많은 경우임
- 여러 car_id들이 있지만 그중 '2022-10-16'에 대여중이 하나라도 있는 car_id들만 따로 서브쿼리로 뺀다음 해당 기존 car_id와 비교하여 해당되면 '대여중', 해당 안되면 '대여 가능'이 나올 수 있게 코딩함.

```sql
select car_id,
    case when car_id in
        (select car_id from CAR_RENTAL_COMPANY_RENTAL_HISTORY 
        where '2022-10-16' between start_date and end_date) then '대여중'
        else '대여 가능' end availability
    from CAR_RENTAL_COMPANY_RENTAL_HISTORY
    group by 1
    order by 1 desc;
```
