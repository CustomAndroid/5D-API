## 获取历史支出

> 用于获取历史支出

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/GetExpenditureHistory`

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
  "startTime": "2018-01-01",
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
| **MonthListvalue** |   int    | 当月 材料支出        |
| **MonthTextFee**   |   int    | 当月 分包支出        |
| **MonthChangeFee** |   int    | 当月 设备支出        |
| **MonthVisaFee**   |   int    | 当月 管理支出        |
| **MonthTotal**     |   int    | （忽略）             |
| **AccListvalue**   |   int    | 累计 材料支出        |
| **AccTextFee**     |   int    | 累计 分包支出        |
| **AccChangeFee**   |   int    | 累计 设备支出        |
| **AccVisaFee**     |   int    | 累计 管理支出        |
| **AccTotal**       |   int    | （忽略）             |

返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": [
    {
      "Projecter": "中铁十二局第二公司",
      "YearMonth": "2018-01",
      "MonthListvalue": 0,
      "MonthTextFee": 0,
      "MonthChangeFee": 0,
      "MonthVisaFee": 0,
      "MonthTotal": 0,
      "AccListvalue": 0,
      "AccTextFee": 0,
      "AccChangeFee": 0,
      "AccVisaFee": 0,
      "AccTotal": 0
    },
    {
      "Projecter": "中铁十二局第二公司",
      "YearMonth": "2018-02",
      "MonthListvalue": 0,
      "MonthTextFee": 0,
      "MonthChangeFee": 0,
      "MonthVisaFee": 0,
      "MonthTotal": 0,
      "AccListvalue": 0,
      "AccTextFee": 0,
      "AccChangeFee": 0,
      "AccVisaFee": 0,
      "AccTotal": 0
    },
    {
      "Projecter": "中铁十二局第二公司",
      "YearMonth": "2018-03",
      "MonthListvalue": 0,
      "MonthTextFee": 0,
      "MonthChangeFee": 0,
      "MonthVisaFee": 0,
      "MonthTotal": 0,
      "AccListvalue": 0,
      "AccTextFee": 0,
      "AccChangeFee": 0,
      "AccVisaFee": 0,
      "AccTotal": 0
    },
    {
      "Projecter": "中铁十二局第二公司",
      "YearMonth": "2018-04",
      "MonthListvalue": 0,
      "MonthTextFee": 0,
      "MonthChangeFee": 0,
      "MonthVisaFee": 0,
      "MonthTotal": 0,
      "AccListvalue": 0,
      "AccTextFee": 0,
      "AccChangeFee": 0,
      "AccVisaFee": 0,
      "AccTotal": 0
    },
    {
      "Projecter": "中铁十二局第二公司",
      "YearMonth": "2018-05",
      "MonthListvalue": 0,
      "MonthTextFee": 0,
      "MonthChangeFee": 0,
      "MonthVisaFee": 0,
      "MonthTotal": 0,
      "AccListvalue": 0,
      "AccTextFee": 0,
      "AccChangeFee": 0,
      "AccVisaFee": 0,
      "AccTotal": 0
    },
    {
      "Projecter": "中铁十二局第二公司",
      "YearMonth": "2018-06",
      "MonthListvalue": 0,
      "MonthTextFee": 0,
      "MonthChangeFee": 0,
      "MonthVisaFee": 0,
      "MonthTotal": 0,
      "AccListvalue": 0,
      "AccTextFee": 0,
      "AccChangeFee": 0,
      "AccVisaFee": 0,
      "AccTotal": 0
    },
    {
      "Projecter": "中铁十二局第二公司",
      "YearMonth": "2018-07",
      "MonthListvalue": 0,
      "MonthTextFee": 0,
      "MonthChangeFee": 0,
      "MonthVisaFee": 0,
      "MonthTotal": 0,
      "AccListvalue": 0,
      "AccTextFee": 0,
      "AccChangeFee": 0,
      "AccVisaFee": 0,
      "AccTotal": 0
    },
    {
      "Projecter": "中铁十二局第二公司",
      "YearMonth": "2018-08",
      "MonthListvalue": 0,
      "MonthTextFee": 0,
      "MonthChangeFee": 0,
      "MonthVisaFee": 0,
      "MonthTotal": 0,
      "AccListvalue": 0,
      "AccTextFee": 0,
      "AccChangeFee": 0,
      "AccVisaFee": 0,
      "AccTotal": 0
    },
    {
      "Projecter": "中铁十二局第二公司",
      "YearMonth": "2018-09",
      "MonthListvalue": 5184,
      "MonthTextFee": 0,
      "MonthChangeFee": 0,
      "MonthVisaFee": 0,
      "MonthTotal": 0,
      "AccListvalue": 5184,
      "AccTextFee": 0,
      "AccChangeFee": 0,
      "AccVisaFee": 0,
      "AccTotal": 0
    },
    {
      "Projecter": "中铁十二局第二公司",
      "YearMonth": "2018-10",
      "MonthListvalue": 0,
      "MonthTextFee": 0,
      "MonthChangeFee": 0,
      "MonthVisaFee": 0,
      "MonthTotal": 0,
      "AccListvalue": 5184,
      "AccTextFee": 0,
      "AccChangeFee": 0,
      "AccVisaFee": 0,
      "AccTotal": 0
    },
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
      "AccTotal": 0
    }
  ]
}
```