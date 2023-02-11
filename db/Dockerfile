FROM debian:latest

RUN apt-get update && apt-get install -y mysql-client

FROM mysql

COPY ./testdump.sql /docker-entrypoint-initdb.d/

ENV MYSQL_DATABASE=student \
    MYSQL_USER=admin \
    MYSQL_PASSWORD=admin123 \
    MYSQL_RANDOM_ROOT_PASSWORD=yes

RUN mysql -h database-1.cbqg2cmmyt06.ap-south-1.rds.amazonaws.com -u admin -padmin123

EXPOSE 3306

