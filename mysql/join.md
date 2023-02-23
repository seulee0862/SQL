링크
https://school.programmers.co.kr/learn/courses/30/lessons/131533

* join문 예시

```mysql
SELECT
    product_code, sum(price*sales_amount) as sales
from
    product p
        join
    offline_sale o_s
    on p.product_id = o_s.product_id
group by
    p.product_code
order by
    sales desc, product_code asc;
```
<br>

* 가상테이블 연습 (같은 내용)
```mysql
WITH a as
(    SELECT
        product_code, sum(price*sales_amount) as sales
    from
        product p
        join
        offline_sale o_s
        on p.product_id = o_s.product_id
    group by
        p.product_code
    order by
    sales desc, product_code asc
 )
select 
    *
from
    a;
```