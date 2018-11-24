## 项目预警列表

> 获取项目预警列表

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/GetWarnings`

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
  "pageIndex": "3",
  "pageSize": "20"
}
```

### 3. 返回参数

| 字段           | 字段类型 | 字段说明                                                     |
| -------------- | :------: | ------------------------------------------------------------ |
| **ID**         |  string  | ID                                                           |
| **CreateTime** |  String  | 时间                                                         |
| **Title**      |  String  | 标题                                                         |
| **Type**       |  String  | 类型：1特种设备 ；2特种人员；3安全隐患；4任务延期；5延期安全隐患 |
| **CreateUser** |  String  | 发起者                                                       |

返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": [
    {
      "Title": "任务延期 Y17中间墩垫石GD_Y17中间墩垫石GD_Y17中间墩垫石GD已延期",
      "CreateTime": "2018/11/24 13:33:45",
      "CreateUser": "系统",
      "Type": "4",
      "ID": "0"
    }
  ]
}
```

