## 整改通知单审核

> 用于整改通知单审核

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/AuditingSafetyRectificationNotice`

### 2. 请求参数

body:

| 字段          | 字段类型 | 必填 | 字段说明                                                     |
| ------------- | :------: | :--: | ------------------------------------------------------------ |
| **projectId** |  String  |  Y   | 项目ID                                                       |
| **userid**    |  String  |  Y   | 用户ID                                                       |
| **type**      |  String  |  Y   | 1标识安全隐患审核，2：标识安全隐患反馈                       |
| **sendTo**    |  String  |  Y   | 发送人                                                       |
| **copyTo**    |  String  |  N   | 抄送人(抄送人中不包含发送人)                                 |
| **id**        |  String  |  Y   | 整改通知单ID                                                 |
| **result**    |  String  |  Y   | 处理结果                                                     |
| **ideas**     |  String  |  Y   | 处理意见                                                     |
| **Step**      |  String  |  Y   | 审核流程步骤，审核列表为空时默认传1，不为空时传最后一次审核的步骤step,即就是最大的。 |

示例:

```json
{
  "userid": "string",
  "projectId": "string",
  "sendTo": "string",
  "copyTo": "string",
  "id": "string",
  "result": "string",
  "ideas": "string",
  "type": "string",
  "Step": "string"
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
  "Datas": null
}
```