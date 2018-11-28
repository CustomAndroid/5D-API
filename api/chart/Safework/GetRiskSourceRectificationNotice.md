## 危险源整改通知单报表

> 用于查询危险源整改通知单报表

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/危险源整改通知单报表`

### 2. 请求参数

body:

| 字段          | 字段类型 | 必填 | 字段说明   |
| ------------- | :------: | :--: | ---------- |
| **userId**    |  String  |  Y   | 用户ID     |
| **projectId** |  String  |  Y   | 项目ID     |
| **startTime** |  String  |  Y   | 开始时间   |
| **endTime**   |  String  |  Y   | 截止时间   |
| **Unit**      |  String  |  N   | 施工单位   |
| **UserType**  |  String  |  Y   | 用户类型ID |



示例:

```json
{
  "userId": "495",
  "projectId": "61",
  "startTime": "2018-11-01",
  "endTime": "2018-11-30",
  "Unit": "437",
  "UserType": "1"
}
```

### 3. 返回参数

| 字段               | 字段类型 | 字段说明             |
| ------------------ | :------: | -------------------- |
| **Code**           |  string  | 0：成功 ；其他：失败 |
| **CodeMsg**        |  String  | 失败时原因信息       |
| **HOrgID**         |          | 施工单位ID           |
| **OrgName**        |          | 施工单位             |
| **StatisDate**     |          | 月份 yyyy-MM         |
| **AllNum**         |          | 发起总量             |
| **NotHandleNum**   |          | 未处理数量           |
| **BeingHandleNum** |          | 正在处理数量         |
| **HaveHandleNum**  |          | 已处理数量           |

返回示例：

```json
{
    "Code": 0, 
    "CodeMsg": "OK", 
    "Datas": [
        {
            "HOrgID": "418", 
            "OrgName": "中铁十二局第二公司", 
            "StatisDate": "2018-11", 
            "AllNum": "0", 
            "NotHandleNum": "0", 
            "BeingHandleNum": "0", 
            "HaveHandleNum": "0"
        }, 
        {
            "HOrgID": "419", 
            "OrgName": "中铁十二局第四公司", 
            "StatisDate": "2018-11", 
            "AllNum": "0", 
            "NotHandleNum": "0", 
            "BeingHandleNum": "0", 
            "HaveHandleNum": "0"
        }
    ]
}
```