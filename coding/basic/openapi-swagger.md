# OpenAPI \(Swagger\)

## 文档

[Swagger Specification](https://swagger.io/docs/specification/)。

## 工具

在 VS Code 中使用插件 [OpenAPI \(Swagger\) Editor](https://marketplace.visualstudio.com/items?itemName=42Crunch.vscode-openapi) 辅助书写，它有智能补全、实时预览（支持 [Swagger UI](https://github.com/swagger-api/swagger-ui) 和 [ReDoc](https://github.com/Redocly/redoc)）、内容索引等能力。

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

![components &#x590D;&#x7528;&#x89C4;&#x5219;](../../.gitbook/assets/b19ecbe3-ea60-45e6-80f1-42021243d8dd.drawio.svg)

1. `path` 可引用 `parameter`, `requestBody`, `response`；
2. `parameter` 可引用 `schema`；
   * 路径参数命名格式 `:<name>`；
3. `response` 可引用 `schema`；
4. `schema` 可引用 `schema`。

另外，`parameter` 和 `requestBody` 注重 `description`。

## 更多

### 空行

借助空行来分隔代码，方便阅读。

![&#x501F;&#x52A9;&#x7A7A;&#x884C;&#x5206;&#x9694;&#x4EE3;&#x7801;](../../.gitbook/assets/eff243b9-4ee5-446e-80db-6a1993428c2d.png)

