# OpenAPI \(Swagger\)

## 文件格式

推荐 `YAML`。辅助字符较少，好写好读。

## Markdown

可用来书写格式化内容或段落。比如，在 `info.description` 中书写前置信息。

![&#x5728; OpenAPI &#x4E2D;&#x4F7F;&#x7528; Markdown](../../.gitbook/assets/f3515eff-88ca-4670-b076-410df1f14c16.png)

## operationId 规则

 `[<parent-resource>:]<resource>:<action>`

| Field | Required | Description |
| :--- | :---: | :--- |
| parent-resource |  | 上级资源。 |
| resource | Y | 资源。 |
| action | Y | 动作，常见的值有 `create`, `index`, `show`, `update`, `delete`。 |

### 例子

* `apps:users:index` - 索引应用中的用户；
* `users:show` - 展示一个用户。

![&#x89C4;&#x5219;&#x7684; operationId](../../.gitbook/assets/a6ca8e55-d92c-4dd7-83e1-883265f5087d.png)

## components 复用规则

* `parameters` 可基于 `schemas`, 被 `paths` 使用；
  * path 型 `parameters` 命名格式 `:<name>`
* `requestBody` 被 `paths` 使用；
* `responses` 可基于 `schemas`, 被 `paths` 使用；
* `schemas` 可基于 `schemas`, 被其他 components 使用（注意不被 `paths` 使用）。

另外，`parameters` 和 `requestBody` 注重 `description`。

## 更多

### 合理借助空行来分隔代码，方便阅读

![&#x501F;&#x52A9;&#x7A7A;&#x884C;&#x5206;&#x9694;&#x4EE3;&#x7801;](../../.gitbook/assets/eff243b9-4ee5-446e-80db-6a1993428c2d.png)



