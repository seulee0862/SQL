링크

https://school.programmers.co.kr/learn/courses/30/lessons/151137

* where 칼럼 regexp ('문자열1|문자열2|...문자열3') -> 문자열 1 ,2 ... 3이 포함된 칼럼검색
* where 칼럼 in ('문자열1|문자열2|..문자열3') -> 문자열 1, 2, 3과 일치하는 칼럼검색
* where 칼럼 like '문자열1' -> 문자열1을 포함한 데이터 검색

```mysql
SELECT
    car_type, count(car_type) car
from
    car_rental_company_car
where
    options regexp '통풍시트|열선시트|가죽시트'
group by
    car_type
order by
    car_type asc;
```