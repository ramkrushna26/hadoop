```
> rm -rf <local path>
> mkdir -p -m 777 <local path>
> hadoop fs -mkdir -p <hadoop path>
> hadoop fs -chmod 777 <hadoop path>
> create hive temporary table
> hadoop fs -getmerge <hadoop files> <local path>
> scp <local path files> <remote path>
> export PGCLIENTENCODING=UTF8;export PGPASSWORD='******';cat <remote file> \
  |psql --host=<db ip> --port=5432 --dbname=<db instance> --username=<db user> -c " COPY <schema>.<table> (<columns>) FROM STDIN WITH NULL '' DELIMITER E',' CSV"
```
