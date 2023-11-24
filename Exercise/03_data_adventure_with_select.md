Explores basic SQL query syntax, including how to sort and filter data.

1. Create a query to retrieve a list of teachers.

- sort the results by school name in ascending alphabetical order.
- ensure that teacher names are listed in A-Z order.

2. create a query for Find teacher who has first_name starting with 's' and earning more than 40000

3. Arrange the teachers in descending order by salary

- including only those who were hired after January 1, 2010. 3.

---

# Answers

1.

```sql
SELECT first_name, school, hire_date
FROM teachers
ORDER By school ASC, hire_date DESC
```

2.

```sql
SELECT * FROM teachers
WHERE first_name ILike 's%'
AND salary > 40000;
```

- point: `Like` operator is case-sensitive while `ILike` in not

3.

```sql
SELECT * FROM teachers
WHERE hire_date < '2010-01-01'
ORDER BY salary DESC;
```

- point: DESC and ASC are correct condition names. there is no condition called DEC
