## 获取未读消息数目

> 获取各类消息未读条目数

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/GetMessageNum`

### 2. 请求参数

body:

| 字段          | 字段类型 | 必填 | 字段说明 |
| ------------- | :------: | :--: | -------- |
| **userid**    |  String  |  Y   | 用户ID   |
| **projectid** |  String  |  Y   | 项目ID   |

示例:

```json
{
  "userid": "496",
  "projectid": "61"
}
```

### 3. 返回参数

| 字段        | 字段类型 | 字段说明                |
| ----------- | :------: | ----------------------- |
| **Message** |  string  | 相关事项未读/未处理数目 |
| **Notice**  |  String  | 通知公告未读/未处理数目 |
| **Todo**    |  String  | 待办未读/未处理数目     |
| **warning** |  String  | 项目预警未读/未处理数目 |

返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": {
    "Message": "0",
    "Notice": "2",
    "Todo": "1",
    "warning": "364"
  }
}
```

