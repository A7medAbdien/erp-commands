# Backup your Database

```sh
mysqldump -u _1bd3e0294da19198 -p _1bd3e0294da19198 > 091824.sql
```

**Notes**:

-   `_9fe7f2edbf963259`: is the database username and the database name
-   `191824.sql`: is the backup file name

# Use SQL backup file

1. login in

```sh
sudo mysql -u _9fe7f2edbf963259 -p
```

2. **Keep the database name stored somewhere**, then drop the current database

```sh
drop database _9fe7f2edbf963259;
```

3. create a database with the same name

```sh
create database _9fe7f2edbf963259;
```

4. logout of mysql by `CTRL` + `Z`

5. use your dump file as source for the new created DB

```sh
mysql -u _9fe7f2edbf963259 -p _9fe7f2edbf963259 < 091824.sql
```
