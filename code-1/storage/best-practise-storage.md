# MySQL

* id binary\(16\) UUID\_TO\_BIN\(UUID\(\)\)
* WHERE id = UUID\_TO\_BIN\(?\)
* Escaping 将参数当作一个值进行转义
* 减少请求 MySQL Server 的次数
* 考虑数据量很大的情况
* 善用索引和缓存

## Guides

* 在 MySQL 中使用 UUID: [Mysql 8.0: UUID support](https://mysqlserverteam.com/mysql-8-0-uuid-support/)。

