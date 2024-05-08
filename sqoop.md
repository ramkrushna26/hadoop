## Sqoop Job Template: for Oracle

```
sqoop import -Dmapred.job.name='job:oracle imports hive' 
--driver oracle.jdbc.driver.OracleDriver 
--connect 'jdbc:oracle:thin:@//10.10.1.1:1521/db' 
--username user_db --password '******' 
--query "SELECT NAME, SALARY, DEPARTMENT, to_char(JOINING_DATE,'yyyy-MM-dd HH24:mi:ss') CONNECTION_DATE, FROM DATABASE.TABLE_EOMPLOYEES WHERE 1=1 AND DEPARTMENT = 'FINANACE' and \$CONDITIONS" 
--delete-target-dir 
--target-dir /tmp/20240301/sqoop_oracle/ 
--fields-terminated-by '|'
--hive-drop-import-delims 
--null-string '' 
--null-non-string '' 
--escaped-by '\\' 
--num-mappers 1
```

## Sqoop Job Template: importing from file to Postgres table
```
sqoop export -Dmapred.job.name='job:hdfs export db<item name>' -Dmapred.job.queue.name=<queue name>
--connect 'jdbc:postgresql://<ip>:<port>/<instance>?gssEncMode=disable' 
--username username
--password '<pwd>' 
--table <target table name>
--num-mappers 1 
--input-null-string '\\N'
--input-null-non-string '\\N' 
--export-dir /tmp/20240507/path/ 
--columns <comma seperated column names>
--fields-terminated-by ","
--schema <schema>
```
