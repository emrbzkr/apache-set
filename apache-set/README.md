# apache-set

## RUN
```
$ docker compose up -d
```

## NiFi
user: admin
password: admin123456789
https://localhost:8443/nifi

## Doris:
user: root
password:
http://localhost:8030

## Superset:
user: admin
password: admin
http://localhost:8088
connect postgresql:
settings > database connections > +Database > PostgreSQL > Connect this database with a SQLALCHEMY URI string instead > postgresql://postgres:postgres@db:5432/superset

## Flink:
http://localhost:8082

## PostgreSQL
localhost:5432
user:postgres
pass: postgres
db: superset
