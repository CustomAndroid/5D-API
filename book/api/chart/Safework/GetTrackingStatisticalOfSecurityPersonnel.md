## 安全员跟踪统计分析

> 用于查询安全员跟踪统计分析

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/GetTrackingStatisticalOfSecurityPersonnel`

### 2. 请求参数

body:

| 字段          | 字段类型 | 必填 | 字段说明 |
| ------------- | :------: | :--: | -------- |
| **projectId** |  String  |  Y   | 项目ID   |
| **startTime** |  String  |  Y   | 开始时间 |
| **endTime**   |  String  |  Y   | 结束时间 |
| **userId**    |  String  |  Y   | 用户ID   |

示例:

```json
{
  "userId": "495",
  "projectId": "61",
  "startTime": "2018-11-01",
  "endTime": "2018-11-30"
}
```

### 3. 返回参数

| 字段           | 字段类型 | 字段说明             |
| -------------- | :------: | -------------------- |
| **Code**       |  string  | 0：成功 ；其他：失败 |
| **CodeMsg**    |  String  | 失败时原因信息       |
| **usercode**   |  String  | 人员ID               |
| **TrueName**   |  String  | 人员名字             |
| **StatisDate** |  String  | 年月                 |
| **lognum**     |  String  | 危险源跟踪次数       |
| **MNum**       |  String  | 发起整改通知单数     |
| **OrgName**    |  String  | 施工单位             |

返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": [
    {
      "usercode": "495",
      "TrueName": "wang1",
      "StatisDate": "2018-11",
      "lognum": "0",
      "MNum": "0",
      "OrgName": "中铁十二局"
    },
    {
      "usercode": "496",
      "TrueName": "wang2",
      "StatisDate": "2018-11",
      "lognum": "0",
      "MNum": "0",
      "OrgName": "中铁十二局第二公司"
    },
    {
      "usercode": "498",
      "TrueName": "wang3",
      "StatisDate": "2018-11",
      "lognum": "0",
      "MNum": "0",
      "OrgName": "贵州桥梁质量检测贵阳分所"
    }
  ]
}
```