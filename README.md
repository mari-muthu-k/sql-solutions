# sql-solutions
## To update the auto-increment default value
### POSTGRES
```
SELECT setval(pg_get_serial_sequence('your_table_name', 'id'), (SELECT MAX(id) FROM your_table_name));
```

### MySQL or MariaDB
```
ALTER TABLE your_table_name AUTO_INCREMENT = new_value;
```
