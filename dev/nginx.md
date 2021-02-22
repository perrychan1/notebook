## nginx

有直接响应的能力，可用来做“就绪检查”。

```nginx
location /ping {
    return 200 'pong';
    add_header Content-Type text/plain;
}
```
