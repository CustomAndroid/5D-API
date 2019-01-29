## 查询危险源监控跟踪列表

> 用于查询危险源监控跟踪列表

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/GetHazardMonitoringTrackingList`

### 2. 请求参数

body:

| 字段          | 字段类型 | 必填 | 字段说明 |
| ------------- | :------: | :--: | -------- |
| **projectid** |  String  |  Y   | 项目ID   |
| **userid**    |  String  |  Y   | 用户ID   |
| **keyword**   |  String  |  N   | 关键字   |

示例:

```json
{
  "userid": "496",
  "projectid": "61",
  "keywords": ""
}
```

### 3. 返回参数

| 字段        | 字段类型 | 字段说明             |
| ----------- | :------: | -------------------- |
| **Code**    |  string  | 0：成功 ；其他：失败 |
| **CodeMsg** |  String  | 失败时原因信息       |
| **Hid**             | String | ID                   |
| **Projectid**       | String | 项目ID               |
| **Title**           | String | 标题                 |
| **SignDate**        | String | 识别时间             |
| **AllNum**          | String | 危险源总数           |
| **ControllableNum** | String | 可控危险源数量       |
| **veryNum**         | String | 异常危险源数量       |
| **Status**          | String | 处理状态             |
| **Adder**           | String | 提报人ID             |
| **Addtime**         | String | 提报时间             |
| **TrueName**        | String | 提报人名字           |

返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": [
    {
      "Hid": "95",
      "Projectid": "61",
      "Title": "电源存在不安全隐患",
      "SignDate": "2018/9/13 0:00:00",
      "Optionid": "495",
      "AllNum": "2",
      "ControllableNum": "0",
      "veryNum": "2",
      "Status": "3",
      "Adder": "wang1",
      "Addtime": "2018/9/13 11:22:14",
      "TrueName": "wang1",
      "rq": "2018/9/19 0:00:00"
    },
    {
      "Hid": "105",
      "Projectid": "61",
      "Title": "危险源识别测试",
      "SignDate": "2018/9/19 0:00:00",
      "Optionid": "495",
      "AllNum": "4",
      "ControllableNum": "4",
      "veryNum": "0",
      "Status": "3",
      "Adder": "wang1",
      "Addtime": "2018/9/19 14:20:37",
      "TrueName": "wang1",
      "rq": ""
    }
  ]
}
```