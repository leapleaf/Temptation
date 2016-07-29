# 更換資料庫密碼

phpMyAdmin請育騰先生改;改好之後參考下列文件:

https://www.evernote.com/shard/s167/sh/0b3e9fe5-eeca-4d16-afe4-b320e30439e7/427112e08be5daaf084ead14b5524edc

設定common/Config.php
```
public static $DBSERVER = "127.0.0.1";
/* Set the name of the database you wish to connect to /
public static $DBNAME = "thechurch"; => temptation
/* set the database user name you wish to use to connect to the database server /
public static $DBUSER = "root";
/* set the password for the username above /
public static $DBPASSWORD = "Local12345"; =>改過的密碼
```
改完後資料庫要重啟