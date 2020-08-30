# leetcode-sql
mysql solution for all leetcode database questions

## question
### 197. Rising Temperature

```
select w1.id from Weather w1, Weather w2

where datediff(w1.recordDate, w2.recordDate) = 1  and w1.temperature > w2.temperature
```

### 595. Big Countries

```
select w.name, w.population, w.area from World w
where w.area>3000000 or w.population>25000000
```

### 596. Classes More Than 5 Students
```
select c.class from (SELECT DISTINCT * FROM courses) AS c
group by c.class 
having count(*) >= 5;
```
Notice that there is no space between count and (*), always be like count(*) 

### 620. Not Boring Movies

```
select id, movie, description, rating from cinema
where (id % 2 != 0) and description != 'boring'
order by rating desc
```

### 627. Swap Salary

```
update salary
SET sex = case when sex='m' then 'f' else 'm' end 
```
Notice that update is followed by the table name
and case when else end is the content that sex equals to.

