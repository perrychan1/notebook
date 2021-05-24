# RESTful API

`action -> object`

向某个对象 `object` 执行某个动作 `action`。借助 HTTP 来表达。

`method -> path`

`method` 表示执行的动作 `action`，`path` 表示接受动作的对象 `object`。例如 `DELETE /users/{id}`。

另外，

* `query`: 查询/过滤条件
* `body`
  * req: 执行动作所需信息
  * res: 执行动作所得结果
* `header`
  * `Accept`: 请求者所期望的执行结果的表现形式，如 `application/json`
  * `Content-Type`
    * req: 请求者执行动作所需信息的展现形式，如 `x-www-form-urlencoded`
    * res: 动作执行所得结果的展现形式，如 `application/json`

## method 与 action 的对应关系

| Method | /users | /users/{id} |
| :---: | :--- | :--- |
| `GET` | 获取全部 `user` | 获取一个 `user` |
| `POST` | 新建一个 `user` | - |
| `PUT` | - | 更新一个 `user` |
| `DELETE` | - | 删除一个 `user` |

## 对象关系的表示

`产品 product` 与`分组 group` 的关系 `/groups/{groupId}/products/{productId}`。

