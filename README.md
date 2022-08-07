# homework4
# 4.1

``` sql
select emp_no,birth_date,first_name,last_name,gender,hire_date
from employees 
order by date(hire_date) desc 
limit 1
```

# 4.2

``` sql
SELECT f.film_id, title
FROM film f LEFT JOIN film_category fc
ON f.film_id = fc.film_id
WHERE last_update IS NULL
```

# 4.3

``` sql
SELECT * 
FROM employees
LIMIT 5, 5;
```

# 4.4

``` sql
ALTER TABLE actor ADD UNIQUE INDEX uniq_idx_firstname(first_name);
ALTER TABLE actor ADD INDEX idx_lastname(last_name);
```

# 4.5

``` sql
SELECT p.id, number, t_rank
FROM passing_number p JOIN (SELECT id, DENSE_RANK() OVER(ORDER BY number DESC) AS t_rank
FROM passing_number) r
ON p.id = r.id
ORDER BY number DESC;
```



