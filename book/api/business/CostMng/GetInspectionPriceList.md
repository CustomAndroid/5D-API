## 查询验工计价台账

> 用于查询验工计价台账

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/GetInspectionPriceList`

### 2. 请求参数

body:

| **参数**                | **数据类型** |  是否必须  | 描述     |
| ------------------------- | :--------: | :--: | ------------------------------------------------------------ |
| **projectId** | **String** |  Y   | 项目ID(审核人)                                               |
| **userId** | String | Y | 用户ID |
| **startTime** | String | Y | 开始时间 |
| **endTime** | String | Y | 截止时间 |
| **Type** | String | Y | 0总包 1分包 |
| **UserType** | String | N | 用户类型 |
| **unit** | String | N | 分包单位，当type=1时 |

示例:

``` json
{
  "userId": "string",
  "projectId": "string",
  "startTime": "string",
  "endTime": "string",
  "unit": "string",
  "Type": "string",
  "UserType": "string"
}
```
### 3. 返回参数

| 字段                      | 字段类型 | 字段说明             |
| ------------------------- | :------: | -------------------- |
| **Code**                  |  string  | 0：成功 ；其他：失败 |
| **CodeMsg**               |  String  | 失败时原因信息       |
| **Lid**                   |  String  | ID                   |
| **projectid**             |  String  | 项目ID               |
| **Ymonth**                |  String  | 年月                 |
| **SubId**                 |  String  | 分包单位             |
| **OrgName**               |  String  | 分包单位名称         |
| **CumulativeValue**       |  String  | 累计完成产值         |
| **CumulativeOutputValue** |  String  | 本月完成产值         |
| **ContractAmount**        |  String  |                      |
| **Listvalue**             |  String  |                      |
| **MeasuresFee**           |  String  |                      |
| **Fees**                  |  String  |                      |
| **SafetyFee**             |  String  | 安全                 |
| **Taxes**                 |  String  |                      |
| **OtherFee**              |  String  |                      |
| **ChangeFee**             |  String  | 变更                 |
| **VisaFee**               |  String  | 签证                 |
| **Type**                  |  String  | 0总包单位 1分包单位  |



返回示例：

```json
{
    "Code": 0, 
    "CodeMsg": "OK", 
    "Datas": [
        {
            "Lid": "84", 
            "projectid": "61", 
            "Ymonth": "2018/9/1 0:00:00", 
            "SubId": "417", 
            "OrgName": "中铁十二局", 
            "CumulativeValue": "56361.90", 
            "CumulativeOutputValue": "57681.90", 
            "ContractAmount": "12000000000.00", 
            "Listvalue": "50309.90", 
            "MeasuresFee": "1000.00", 
            "Fees": "1000.00", 
            "SafetyFee": "1411.00", 
            "Taxes": "1200.00", 
            "OtherFee": "1441.00", 
            "ChangeFee": "1320.00", 
            "VisaFee": "0.00", 
            "Type": "1"
        }
    ]
}
```