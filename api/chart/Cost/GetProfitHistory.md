## 获取历史利润

> 用于获取历史利润 （一年）

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/GetProfitHistory`

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
| **MonthListvalue** |   int    | 当月 账面收入        |
| **MonthTextFee**   |   int    | 当月 实际收入        |
| **MonthChangeFee** |   int    | 当月 应收            |
| **MonthVisaFee**   |   int    | 当月 支出            |
| **MonthTotal**     |   int    | 当月 实际利润        |
| **AccListvalue**   |   int    | 累计 账面收入        |
| **AccTextFee**     |   int    | 累计 实际收入        |
| **AccChangeFee**   |   int    | 累计 应收            |
| **AccVisaFee**     |   int    | 累计 支出            |
| **AccTotal**       |   int    | 累计 实际利润        |

``` js
var MonthTotalZ = decimal.Parse(item.MonthListvalue.ToString()) - decimal.Parse(item.MonthVisaFee.ToString());//当月账面利润 = MonthListvalue-MonthVisaFee
var AccTotalZ = decimal.Parse(item.AccListvalue.ToString()) - decimal.Parse(item.AccVisaFee.ToString());//累计账面利润 = AccListvalue-AccVisaFee
```



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
      "MonthListvalue": 26015,
      "MonthTextFee": 0,
      "MonthChangeFee": 26015,
      "MonthVisaFee": 5184,
      "MonthTotal": 0,
      "AccListvalue": 26015,
      "AccTextFee": 0,
      "AccChangeFee": 26015,
      "AccVisaFee": 5184,
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
      "AccListvalue": 26015,
      "AccTextFee": 0,
      "AccChangeFee": 26015,
      "AccVisaFee": 5184,
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
      "AccListvalue": 26015,
      "AccTextFee": 0,
      "AccChangeFee": 26015,
      "AccVisaFee": 5184,
      "AccTotal": 0
    }
  ]
}
```