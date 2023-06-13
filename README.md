
# Apach + PHP:7.4 + MYSQL + PHPMyAdmin 

## Docker-compose.yml

This image is intended for PHP+MySQL development.  

``` docker compose up ``` 

``` docker compose down ```

Both MySQL and phpmyadmin use **passwords** intended in docker-compose.yml file.

**Mysqli, pdo, pdo_mysql** are also installed as dependencies to work with PDO driver from php code.

- This image uses ``/www`` directory for your page files.
- This image uses ``/dump`` directory for database initialization files.

When MSQL container is started for the first time, a new database with the specified name will be created and initialized with the provided configuration variables. It will execute files with extensions .sh, .sql and .sql.gz that are found in /dump. 
 You can populate your mysql services by mounting a SQL dump into that directory and provide custom images with contributed data. SQL files will be imported by default to the database specified by the MYSQL_DATABASE variable.