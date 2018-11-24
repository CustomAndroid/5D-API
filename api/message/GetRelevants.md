## 相关事项列表

> 获取相关事项列表

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/GetRelevants`

### 2. 请求参数

body:

| 字段          | 字段类型 | 必填 | 字段说明 |
| ------------- | :------: | :--: | -------- |
| **userid**    |  String  |  Y   | 用户ID   |
| **projectid** |  String  |  Y   | 项目ID   |
| **pageIndex** |  String  |  Y   | 页码     |
| **pageSize**  |  String  |  Y   | 每页条数 |

示例:

```json
{
  "userid": "496",
  "projectid": "61",
  "pageIndex": "1",
  "pageSize": "20"
}
```

### 3. 返回参数

| 字段           | 字段类型 | 字段说明                                          |
| -------------- | :------: | ------------------------------------------------- |
| **ID**         |  string  | ID                                                |
| **CreateTime** |  String  | 时间                                              |
| **Title**      |  String  | 标题                                              |
| **Type**       |  String  | 类型：参考[待办事项消息类型](getTODOs.md#4. 附录) |
| **CreateUser** |  String  | 发起者                                            |

返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": [
    {
      "CreateUser": "wang1",
      "CreateTime": "2018/11/22 11:27:00",
      "Title": "有危险源识别需要您的查阅,标题为:11-22危险源识别测试",
      "Type": "17",
      "ID": "107",
      "ExtendID": "7f01783c-23f8-4c8a-aa70-17b1e0c37913"
    }
  ],
  "Count": 1
}
```

