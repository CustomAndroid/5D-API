## 查询问题审批处理进度

> 用于查询问题审批处理进度

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/getQualityCheckProcess`

### 2. 请求参数

body:

| 字段       | 字段类型 | 必填 | 字段说明 |
| ---------- | :------: | :--: | -------- |
| **userId** |  String  |  Y   | 用户ID   |
| **quesId** |  String  |  Y   | 问题ID   |

示例:

```json
{
  "userId": "495",
  "quesId": "129"
}
```

### 3. 返回参数

| 字段           |  类型  | 字段说明                                                     |
| -------------- | :----: | ------------------------------------------------------------ |
| **Code**       | string | 0：成功 ；其他：失败                                         |
| **CodeMsg**    | String | 失败时原因信息                                               |
| **auditor**    | String | 审核人                                                       |
| **reportTime** | String | 审核时间                                                     |
| **statusName** | String | 处理意见                                                     |
| **result**     | String | 处理结果                                                     |
| **desc**       | String | 处理措施                                                     |
| **status**     | String | 状态 ：1待审（等待`auditor`审核，待审时`statusName`、`result`、`desc`都是空的）， 2已审（已由`auditor`审核） |
| **Lid**        | String | 流程ID                                                       |



返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": [
    {
      "auditor": "wang1",
      "reportTime": "2018-11-28",
      "statusName": "",
      "result": "",
      "desc": "",
      "status": "2",
      "Lid": "201"
    }
  ]
}
```

