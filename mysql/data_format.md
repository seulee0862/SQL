링크
https://school.programmers.co.kr/learn/courses/30/lessons/131120

* date_format(date_of_birth,'%Y-%m-%d') 복습
* 조건만 잘 읽으면 실수할게 없음

```mysql
SELECT
    member_id, member_name, gender, date_format(date_of_birth,'%Y-%m-%d') date_of_birth
from
    member_profile
where 
    date_format(date_of_birth, '%m') = '03'
    and
    gender = 'W'
    and
    tlno is not null
order by
    member_id asc
```