## 获取当月收入

> 用于获取当月收入

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/GetIncomeStatistics`

### 2. 请求参数

body:

| 字段          | 字段类型 | 必填 | 字段说明            |
| ------------- | :------: | :--: | ------------------- |
| **projectid** |  String  |  Y   | 项目ID              |
| **usercode**  |  String  |  Y   | 用户ID              |
| **startTime** |  String  |  Y   | 开始时间 yyyy-MM-dd |
| **endTime**   |  String  |  Y   | 截止时间 yyyy-MM-dd |

示例:

```json
{
  "projectid": "61",
  "usercode": "496",
  "startTime": "2018-11-01",
  "endTime": "2018-11-30"
}
```

### 3. 返回参数

| 字段               | 字段类型 | 字段说明             |
| ------------------ | :------: | -------------------- |
| **Code**           |  string  | 0：成功 ；其他：失败 |
| **CodeMsg**        |  String  | 失败时原因信息       |
| **Projecter**      |  String  | 施工单位             |
| **YearMonth**      |  String  | 年月                 |
| **MonthListvalue** |   int    | 当月 工程量          |
| **MonthTextFee**   |   int    | 当月 税费规费等      |
| **MonthChangeFee** |   int    | 当月 变更费用        |
| **MonthVisaFee**   |   int    | 当月 签证费用        |
| **MonthTotal**     |   int    | 当月 合计            |
| **AccListvalue**   |   int    | 累计 工程量          |
| **AccTextFee**     |   int    | 累计 税费规费等      |
| **AccChangeFee**   |   int    | 累计 变更费用        |
| **AccVisaFee**     |   int    | 累计 签证费用        |
| **AccTotal**       |   int    | 累计 合计            |

返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": [
    {
      "Projecter": "中铁十二局第二公司",
      "YearMonth": "2018-11",
      "MonthListvalue": 0,
      "MonthTextFee": 0,
      "MonthChangeFee": 0,
      "MonthVisaFee": 0,
      "MonthTotal": 0,
      "AccListvalue": 5184,
      "AccTextFee": 0,
      "AccChangeFee": 0,
      "AccVisaFee": 0,
      "AccTotal": 5184
    }
  ]
}
```