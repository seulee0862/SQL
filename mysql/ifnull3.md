링크
https://school.programmers.co.kr/learn/courses/30/lessons/132201

* ifnull(칼럼, 'A') -> 칼럼값이 null이면 A로출력

```mysql
SELECT
    pt_name, pt_no, gend_cd, age, ifnull(tlno, 'NONE') as tlno
from
    patient
where
    gend_cd = 'W'
  and age <= 12
order by
    age desc, pt_name asc
```
