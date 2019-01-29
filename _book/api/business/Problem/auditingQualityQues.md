## 问题审核

> 用于问题审核

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/auditingQualityQues`

### 2. 请求参数

body:

| 字段            | 字段类型 | 必填 | 字段说明                                                     |
| --------------- | :------: | :--: | ------------------------------------------------------------ |
| **userId**      |  String  |  Y   | 用户ID                                                       |
| **qualityQues** |  String  |  Y   | 问题ID                                                       |
| **qStepId**     |  String  |  Y   | 问题处理步骤ID（从[getQualityCheckProcess](getQualityCheckProcess.md)接口获取最后一条的`Lid`） |
| **qResult**     |  String  |  Y   | 处理结果                                                     |
| **qIdea**       |  String  |  Y   | 处理意见                                                     |
| **qComment**    |  String  |  N   | 处理措施                                                     |
| **sendTo**      |  String  |  Y   | 发送人                                                       |
| **copyTo**      |  String  |  N   | 抄送人                                                       |
| **IsFirst**     |  String  |  Y   | 0代表关闭，1代表审核提交                                     |

示例:

```json
{
  "userId": "string",
  "qualityQues": "string",
  "qStepId": "string",
  "qResult": "string",
  "qIdea": "string",
  "qComment": "string",
  "sendTo": "string",
  "copyTo": "string",
  "IsFirst": "string"
}
```

### 3. 返回参数

| 字段        |  类型  | 字段说明             |
| ----------- | :----: | -------------------- |
| **Code**    | string | 0：成功 ；其他：失败 |
| **CodeMsg** | String | 失败时原因信息       |



返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": null
}
```

