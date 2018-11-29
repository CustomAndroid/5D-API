## 变更台账

> 用于查询变更台账

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/GetChangeBook`

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
  "unit": "string",
  "Type": "string",
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
            "ID": "52", 
            "ProjectId": "61", 
            "ChangeCode": "G20180908113647659", 
            "ContractName": "中铁十二局第四公司合同", 
            "PName": "", 
            "ConstructionID": "419", 
            "ConstructionName": "中铁十二局第四公司", 
            "Site": "引桥_引桥", 
            "AmountWork": "1600.00", 
            "AmountUnit": "3", 
            "Price": "1200.00", 
            "Amount": "1920000.00", 
            "ContractAmount": "60000000.00", 
            "Dish": "417", 
            "ApplicantDate": "2018/9/8 11:38:37", 
            "Status": "3", 
            "CurrExecuteId": "495", 
            "ReviewIds": "", 
            "Mid": "600_646800,600_648898,600_651210,600_652617,600_654518,600_655449,600_656991,600_658209,600_658905,600_659490,600_660053,600_660596,600_662037,600_662558,600_663077,600_663592,600_943791", 
            "JStatus": "3"
        }
    ]
}
```