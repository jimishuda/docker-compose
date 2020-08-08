

#### 本地启动一个MYSQL
```shell
docker run -p 3306:3306 --name mysql -e MYSQL_ROOT_PASSWORD=root -d mysql:5.7
```
配置root远程连接
```sql
mysql -uroot -proot
use mysql;
select user,authentication_string,host from user;
GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' IDENTIFIED BY 'root';
flush privileges;
```
