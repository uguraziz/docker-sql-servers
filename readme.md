# Database Setup Using Docker

This document contains Docker commands to set up MySQL, MSSQL, and PostgreSQL databases.

## MySQL

To run a MySQL container:

```bash
docker run --name mysql -e MYSQL_ROOT_PASSWORD=Password1 -p 3306:3306 -v mysql-data:/var/lib/mysql -d mysql:latest
```

- MYSQL_RO- OT_PASSWORD: The root password for MySQL.
- MYSQL_DATABASE: The name of the database to be created.

#####  Connecting to MySQL
1. Host: localhost
2. Port: 3306
3. User: root
4. Password: Password1


## MSSQL

To run a MSSQL container:

```bash
docker run -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=Password1" -p 1433:1433 --name mssql -v sqlserverdata:/var/opt/mssql -d mcr.microsoft.com/mssql/server:2022-latest
```

- ACCEPT_EULA: Set to "Y" to accept the MSSQL EULA.
- SA_PASSWORD: The system administrator password for MSSQL.

#####  Connecting to MSSQL
1. Host: localhost
2. Port: 1433
3. User: sa
4. Password: Password1

## PostgreSQL

To run a PostgreSQL container:

```bash
docker run --name postgres -e POSTGRES_PASSWORD=Password1 -p 5432:5432 -v postgres-data:/var/lib/postgresql/data -d postgres:latest
```

- POSTGRES_PASSWORD: The password for the PostgreSQL user.
- POSTGRES_DB: The name of the database to be created.

#####  Connecting to PostgreSQL
1. Host: localhost
2. Port: 5432
3. User: postgres
4. Password: Password1
