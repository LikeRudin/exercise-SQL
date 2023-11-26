### Failed Query

```sql
COPY char_data_types TO 'C:\Users\typetest.txt'
WITH (FORMAT CSV, HEADER, DELIMITER '|');
```

ERROR: relative path not allowed for COPY to file

SQL state: 42602

```sql
COPY char_data_types TO '/mnt/c/Users/data_types.txt'
WITH (FORMAT CSV, HEADER, DELIMITER '|');
```

ERROR: could not open file "/mnt/c/Users/data_types.txt" for writing: Permission denied
HINT: COPY TO instructs the PostgreSQL server process to write a file. You may want a client-side facility such as psql's \copy.

- There is a permission problem. I am accessing Windows' file path, but pgAdmin and PostgreSQL are running on the Linux subsystem for Windows which is the reason i am guessing for Error

### Evade Problem

```sql
COPY teachers TO '/tmp/data_types.txt'
WITH (FORMAT CSV, HEADER, DELIMITER '|');
```

Used tmp directory which is allowed for everone to access

- need futher study
