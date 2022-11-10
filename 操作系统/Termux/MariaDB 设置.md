# Termux MariaDB 设置

## [设置 root 用户](https://wiki.termux.com/wiki/MariaDB)

以当前 Termux 用户登录:

```sh
mysql -u `whoami`
```

手动设置 root 用户密码:

```sql
USE mysql;
SET PASSWORD FOR 'root'@'localhost' = PASSWORD('YOUR_ROOT_PASSWORD_HERE');
FLUSH PRIVILEGES;
QUIT;
```

## Termux 修改 MariaDB 编码为 utf8md4

### 修改全局设置

在 `$PREFIX/etc/my.cnf` 中添加：

```ini
[client]
default-character-set = utf8mb4

[mysql]
default-character-set = utf8mb4

[mysqld]
character-set-client-handshake = FALSE
character-set-server = utf8mb4
collation-server = utf8mb4_unicode_ci
init_connect = 'SET NAMES utf8mb4'
```

重启数据库。

查看编码；

```mysql
SHOW VARIABLES WHERE variable_name LIKE 'character_set_%' OR variable_name LIKE 'collation%';
```

### 修改数据库编码

```mysql
ALTER DATABASE database_name CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci;
```

### 修改数据表编码

```mysql
ALTER TABLE table_name
    CONVERT TO CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci;
```
