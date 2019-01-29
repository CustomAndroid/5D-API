## 签证台账

> 用于查询签证台账

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/GetVisaStandingBookList`

### 2. 请求参数

body:

| **参数**                | **数据类型** |  是否必须  | 描述     |
| ------------------------- | :--------: | :--: | ------------------------------------------------------------ |
| **projectId** | **String** |  Y   | 项目ID(审核人)                                               |
| **userId** | String | Y | 用户ID |
| **UserType** | String | N | 用户类型ID |
| **startTime** | String | Y | 开始时间 |
| **endTime** | String | Y | 截止时间 |
| **unit** | String | N | 0 |
| **Type** | String | N | 0 |

示例:

``` json
{
  "userId": "string",
  "projectId": "string",
  "startTime": "string",
  "endTime": "string",
  "unit": "0",
  "Status": "0",
  "UserType": "string"
}
```
### 3. 返回参数

| 字段                 | 字段类型 | 字段说明             |
| -------------------- | :------: | -------------------- |
| **Code**             |  string  | 0：成功 ；其他：失败 |
| **CodeMsg**          |  String  | 失败时原因信息       |
| **ID**               |          | 变更ID               |
| **ProjectId**        |          | 项目ID               |
| **ChangeCode**       |          | 变更编号             |
| **ContractName**     |          | 合同名称             |
| **ConstructionID**   |          | 施工单位             |
| **ConstructionName** |          | 施工单位名称         |
| **Site**             |          | 变更部位             |
| **ApplicantDate**    |          | 日期                 |
| **Mid**              |          | 构件ID               |
| **Status**           |          | 流程状态             |
| **JStatus**          |          | 结算状态             |
| **ContractAmount**   |          | 合同金额             |
| **AmountWork**       |          |                      |
| **Price**            |          | 单价                 |
| **Amount**           |          | 总价                 |



返回示例：

```json
{
    "Code": 0, 
    "CodeMsg": "OK", 
    "Datas": [
        {
            "ID": "36", 
            "ProjectId": "61", 
            "ContractName": "总包合同001", 
            "PName": "", 
            "ConstructionID": "417", 
            "ConstructionName": "中铁十二局", 
            "Site": "引桥_引桥", 
            "AmountWork": "0.00", 
            "AmountUnit": "0", 
            "Price": "0.00", 
            "Amount": "123.00", 
            "ContractAmount": "12000000000.00", 
            "Dish": "417", 
            "ApplicantDate": "2018/10/15 17:31:57", 
            "Status": "1", 
            "CurrExecuteId": "498", 
            "ReviewIds": "", 
            "JStatus": "1"
        }
    ]
}
```