### Failed Query

```sql
INSERT INTO teachers
VALUES(first_name = "yj",
	  last_name="s",
	  school="self study",
	  hire_date=2023-11-24,
	  salary=555);
```

- Before checking the answer, think about what is the wrong with the above query

ERROR: There is a column named "first_name" in table "teachers", but it cannot be referenced from this part of the query.column "first_name" does not exist

ERROR: date/time field value out of range: "23-11-24"
LINE 2: VALUES('yj', 's', 'self studying', '23-11-24', 9620)

### Answer

```
INSERT INTO teachers(first_name,last_name,school,hire_date,salary)
VALUES('yj', 's', 'self studying', '2023-11-24', 9620)
```

1. Syntax Error:

   - column
     - should write colums on right of table name
     - should wrap values for column with `''` not `""`

2. Value Error:

   - must Write 4 numbers for year in column type - date/time
