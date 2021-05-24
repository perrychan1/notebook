# MySQL

* id binary\(16\) UUID\_TO\_BIN\(UUID\(\)\)
  * WHERE id = UUID\_TO\_BIN\(?\)
* Escaping 将参数当作一个值进行转义
* 减少请求 MySQL Server 的次数
* 考虑数据量很大的情况
* 善用索引和缓存

## Docker

```bash
docker run -d \
--name mysql \
-e LANG=C.UTF-8 \
-e MYSQL_ALLOW_EMPTY_PASSWORD=yes \
-v mysql:/var/lib/mysql \
-p 3306:3306 \
--restart always \
mysql:5.7 \
--character-set-server=utf8mb4 \
--collation-server=utf8mb4_unicode_ci
```

Use env `LANG` to support typing Chineses. It comes from base image [debian](https://hub.docker.com/_/debian#locales).

## Guides

* 在 MySQL 中使用 UUID: [Mysql 8.0: UUID support](https://mysqlserverteam.com/mysql-8-0-uuid-support/)。

