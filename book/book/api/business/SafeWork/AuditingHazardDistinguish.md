## 危险源识别审核

> 用于危险源识别审核

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/AuditingHazardDistinguish`

### 2. 请求参数

body:

| 字段               | 字段类型 | 必填 | 字段说明     |
| ------------------ | :------: | :--: | ------------ |
| **projectid**      |  String  |  Y   | 项目ID       |
| **userid**         |  String  |  Y   | 用户ID       |
| **id**             |  String  |  Y   | 危险源识别ID |
| **result**         |  String  |  Y   | 处理结果     |
| **ideas**          |  String  |  Y   | 处理意见     |
| **measures**       |  String  |  N   | 处理措施     |
| **sendTo**         |  String  |  N   | 发送人       |
| **copyTo**         |  String  |  N   | 相关人       |
| ~~**IsSendNext**~~ |  String  |  N   | (无用)       |
| **Type**           |  String  |  Y   | 1审核  2反馈 |

示例:

```json
{
  "userid": "string",
  "projectid": "string",
  "id": "string",
  "result": "string",
  "ideas": "string",
  "measures": "string",
  "sendTo": "string",
  "copyTo": "string",
  "IsSendNext": "string",
  "Type": "string"
}
```

### 3. 返回参数

| 字段        | 字段类型 | 字段说明             |
| ----------- | :------: | -------------------- |
| **Code**    |  string  | 0：成功 ；其他：失败 |
| **CodeMsg** |  String  | 失败时原因信息       |

返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas":null
}
```