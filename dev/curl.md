# curl

```bash
curl 'www.example.com' \
-X POST \
-H 'Cookie: PHPSESSID=298zf09hf012fh2; csrftoken=u32t4o3tb3gg43;' \
-H 'Content-Type: x-www-form-urlencoded' \
-d 'page=0&pageSize=10' \
```

* `-d`: data, HTTP body
* `-H`: HTTP Header
* `-L`: 跟随 301 重定向
* `-O`: 输出到 basename 同名文件
* `-o=file.txt`: 输出到文件
* `-X`: HTTP method
* `-I`: 仅输出 response Header
* `--trace-ascii /dev/stdout`: show request body

