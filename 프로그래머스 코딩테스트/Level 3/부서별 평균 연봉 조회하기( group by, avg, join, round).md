
![20240318_174428](https://github.com/junhosong0/MySQL/assets/117610783/57775408-0da1-4438-b3c1-6aa09fc63156)

![20240318_174444](https://github.com/junhosong0/MySQL/assets/117610783/a825daaf-7966-456c-80d7-fc1a4f480c54)




**내코드**
- join하고 평균을 구할 조건 컬럼을 group by 해줘서 select절에서 avg를 통해 평균값 구해줌
- 나머지 조건을들 round와 order by 절로 해줌

```sql
select dept_id, dept_name_en, round(avg(sal), 0) as AVG_SAL
from hr_department d
join hr_employees e using(dept_id)
group by dept_id
order by AVG_SAL desc
```




**배울것**
- join 절 없이 푸는 법. from절에 두개 테이블 선언 해주고 where 절에서 조인에서 on 조건과 동일한 값을 넣어줌

```sql
SELECT E.DEPT_ID, DEPT_NAME_EN, ROUND(AVG(SAL), 0) AS AVG_SAL
FROM HR_DEPARTMENT D, HR_EMPLOYEES E
WHERE D.DEPT_ID = E.DEPT_ID
GROUP BY E.DEPT_ID
ORDER BY AVG_SAL DESC;"

```
