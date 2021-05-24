# docker

## nginx

```bash
# send `HUP` signal to container
# nginx reload config file
docker kill -s HUP nginx-container-name
```

## MySQL

```bash
# 解决终端无法键入中文的问题
docker run --name mysql -d \
-e LANG=C.UTF-8 \
-e MYSQL_ROOT_PASSWORD=secret \
-v mysql:/var/lib/mysql \
-p 3306:3306 \
--restart always \
mysql:5.7 \
--character-set-server=utf8mb4 \
--collation-server=utf8mb4_unicode_ci
```

参考 [Docker Hub](https://hub.docker.com/_/debian#locales).

## Signal

Docker 向 Container 发送 `SIGTERM` 以终止它。

