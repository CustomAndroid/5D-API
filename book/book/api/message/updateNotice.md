## 通知公告标记已读

> 更改通知公告未读状态为已读

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/updateNotice`

### 2. 请求参数

body:

| 字段          | 字段类型 | 必填 | 字段说明                                      |
| ------------- | :------: | :--: | --------------------------------------------- |
| **userid**    |  String  |  Y   | 用户ID                                        |
| **projectid** |  String  |  Y   | 项目ID                                        |
| **caseId**    |  String  |  Y   | 通知公告的ID，来自于[通知公告](getNotices.md) |

示例:

```json
{
  "userId": "string",
  "projectID": "string",
  "caseId": "string"
}
```

### 3. 返回参数

| 字段        | 字段类型 | 字段说明          |
| ----------- | :------: | ----------------- |
| **Code**    |  string  | 0 成功， 其他失败 |
| **CodeMsg** |  String  | 失败时原因信息    |

返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "",
  "Datas": null
}
```

