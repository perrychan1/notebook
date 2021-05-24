# MySQL

* id binary\(16\) UUID\_TO\_BIN\(UUID\(\)\)
* WHERE id = UUID\_TO\_BIN\(?\)
* Escaping 将参数当作一个值进行转义
* 减少请求 MySQL Server 的次数
* 考虑数据量很大的情况
* 善用索引和缓存

