### Failed Query

1.

```sql
SELECT * from teachers
ORDER BY school, first_name AS ASC;
```

ERROR: syntax error at or near "AS"
LINE 2: ORDER BY school, first_name AS ASC;

2.

```sql
SELECT * FROM teachers
WHERE hire_date < '2010-01-01'
ORDER BY salary DEC;
```

---

### Answer

1.

```sql
SELECT * from teachers
ORDER BY school, first_name ASC;
```

- There is nothing between column name and order condition.
  - `AS` Created an Error

2.

```sql
SELECT * FROM teachers
WHERE hire_date < '2010-01-01'
ORDER BY salary DESC;
```

- DESC and ASC are correct condition names
