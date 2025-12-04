# Montagem de ambiente
## Postgresql
#### documentação: https://hub.docker.com/_/postgres
```docker run --name RHP_DW -p 5437:5432 -e POSTGRES_USER=rhp -e POSTGRES_PASSWORD=rhp1010 -e POSTGRES_DB=rhp_dw -d postgres:16.0```

## Mysql
#### documentação: https://hub.docker.com/_/mysql
```docker run --name DB_FORNECEDOR_1 -p 3306:3306 -e MYSQL_USER=rhp -e MYSQL_PASSWORD=fornecedor1 -e MYSQL_DATABASE=rhp_dados -e MYSQL_RANDOM_ROOT_PASSWORD=yes -d mysql:9.5.0```
#### para conectar, modifique: allowPublicKeyRetrieval=TRUE

## MariaDB
#### documentação: https://hub.docker.com/_/mariadb
```docker run --name DB_FORNECEDOR_2 -p 3307:3306 -e MARIADB_RANDOM_ROOT_PASSWORD=1 -e MARIADB_USER=rhp -e MARIADB_PASSWORD=fornecedor2 -e MARIADB_DATABASE=rhp_dados2 mariadb:12.2.1```