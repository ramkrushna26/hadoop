## Sqoop job template

```
sqoop import -Dmapred.job.name='job:oracle imports hive|workitemId:171234|taskId:123|acct:12345' 
--driver oracle.jdbc.driver.OracleDriver 
--connect 'jdbc:oracle:thin:@//10.10.1.1:1521/db' 
--username user_db --password '******' 
--query "SELECT NAME, SALARY, DEPARTMENT, to_char(JOINING_DATE,'yyyy-MM-dd HH24:mi:ss') CONNECTION_DATE, FROM DATABASE.TABLE_EOMPLOYEES WHERE 1=1 AND DEPARTMENT = 'FINANACE' and \$CONDITIONS" 
--delete-target-dir 
--target-dir /tmp/ditagent/20240301/sqoop_oracle_0e0a5436a1ce48a6bdec69b0fad68aef/ 
--fields-terminated-by '' 
--hive-drop-import-delims 
--null-string '' 
--null-non-string '' 
--escaped-by '\\' 
--num-mappers 1
```
