## 危险源统计分析

> 用于查询危险源统计分析

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/GetStatisticalAnalysisOfHazardSources`

### 2. 请求参数

body:

| 字段          | 字段类型 | 必填 | 字段说明   |
| ------------- | :------: | :--: | ---------- |
| **projectId** |  String  |  Y   | 项目ID     |
| **startTime** |  String  |  Y   | 开始时间   |
| **endTime**   |  String  |  Y   | 结束时间   |
| **userId**    |  String  |  Y   | 用户ID     |
| **unit**      |  String  |  Y   | 施工单位ID |
| **UserType**  |  String  |  Y   | 用户类型   |

示例:

```json
{
  "userId": "496",
  "projectId": "61",
  "startTime": "2018-11-01",
  "endTime": "2018-11-30",
  "unit": "418",
  "UserType": "2"
}
```

### 3. 返回参数

| 字段         | 字段类型 | 字段说明             |
| ------------ | :------: | -------------------- |
| **Code**     |  string  | 0：成功 ；其他：失败 |
| **CodeMsg**  |  String  | 失败时原因信息       |
| **allnum**   |  String  | 发起总数             |
| **lognum**   |  String  | 已处理数量           |
| **errornum** |  String  | 正在处理数量         |
| **Unnum**    |  String  | 未处理数量           |
| **HOrgID**   |  String  | 施工单位ID           |
| **OrgName**  |  String  | 施工单位             |

返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": [
    {
      "allnum": "0",
      "lognum": "0",
      "errornum": "0",
      "Unnum": "0",
      "HOrgID": "418",
      "OrgName": "中铁十二局第二公司"
    }
  ]
}
```