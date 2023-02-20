링크
https://school.programmers.co.kr/learn/courses/30/lessons/132202

* DATE_FORMAT을통한 특정월검색
* 문법 실행순서 한번 상기시키기 좋은 문제라고 생각함<br>
  SELECT -> FROM -> WHERE -> GROUP BY -> HAVING -> ORDER BY

```mysql
SELECT
    mcdp_cd 진료과코드, count(mcdp_cd) 5월예약건수
from
    appointment
where
    date_format(apnt_ymd, '%Y-%m') = '2022-05'
group by
    mcdp_cd
order by
    count(mcdp_cd) asc, mcdp_cd asc
```