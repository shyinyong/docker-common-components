docker-compose.exe down
docker-compose.exe up -d

docker-compose.exe rm -v
docker volume prune

mysql 修改密码后， 重新删除 mysql data, docker 相关的mysql的数据

GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' IDENTIFIED BY '123456';
FLUSH PRIVILEGES;

GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' IDENTIFIED BY '123456' WITH GRANT OPTION;
FLUSH PRIVILEGES;

ALTER USER 'root'@'%' IDENTIFIED WITH mysql_native_password BY '123456';
FLUSH PRIVILEGES;

mysql 8.0 版本
更改 MySQL 用户的身份验证方法为 mysql_native_password

ALTER USER 'root'@'%' IDENTIFIED WITH mysql_native_password BY '123456';
FLUSH PRIVILEGES;
