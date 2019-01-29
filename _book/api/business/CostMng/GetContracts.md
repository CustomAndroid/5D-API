## 合同查询

> 用于合同查询

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/GetContracts`

### 2. 请求参数

body:

| **参数**                | **数据类型** |  是否必须  | 描述     |
| ------------------------- | :--------: | :--: | ------------------------------------------------------------ |
| **projectId** | **String** |  Y   | 项目ID(审核人)                                               |
| **userId** | String | Y | 用户ID |
| **model** | String | Y | 合同模式，来自[getBaseData](../../project/getBaseData.md)中`ContractMode`类型 |
| **keywords** | String | Y | 关键字 |
| **UserType** | String | N | 用户类型 |
| **unit** | String | N | 施工单位 |

示例:

``` json
{
  "userId": "string",
  "projectId": "string",
  "model": "string",
  "keywords": "string",
  "UserType": "string",
  "unit": "string"
}
```
### 3. 返回参数

| 字段                  | 字段类型 | 字段说明                                                     |
| --------------------- | :------: | ------------------------------------------------------------ |
| **Code**              |  string  | 0：成功 ；其他：失败                                         |
| **CodeMsg**           |  String  | 失败时原因信息                                               |
| **Cid**               |  String  | 合同ID                                                       |
| **Employer**          |  String  | 发包方                                                       |
| **Contractor**        |  String  | 承包方                                                       |
| **ContractMode**      |  String  | 合同模式，来自[getBaseData](../../project/getBaseData.md)中`ContractMode`类型 |
| **ContractCode**      |  String  | 合同编号                                                     |
| **ContractName**      |  String  | 合同名称                                                     |
| **ContractAmount**    |  String  | 合同金额(元)                                                 |
| **starDate**          |  String  | 开始时间                                                     |
| **EndDate**           |  String  | 截止时间                                                     |
| **Note**              |  String  | 备注                                                         |
| **Adddate**           |  String  | 添加时间                                                     |
| **Adder**             |  String  | 提报人                                                       |
| **Usercode**          |  String  | 提报人ID                                                     |
| **projectid**         |  String  | 项目ID                                                       |
| **SafeFee**           |  String  | 安全文明施工费(元)                                           |
| **ContractModelName** |  String  | 合同模式名称                                                 |



返回示例：

```json
{
    "Code": 0, 
    "CodeMsg": "OK", 
    "Datas": [
        {
            "Cid": "96", 
            "Employer": "416", 
            "Contractor": "417", 
            "ContractMode": "2", 
            "ContractCode": "Z201809001", 
            "ContractName": "总包合同001", 
            "ContractAmount": "12000000000.00", 
            "starDate": "2018/9/8 0:00:00", 
            "EndDate": "2021/12/31 0:00:00", 
            "Note": "", 
            "Adddate": "2018/9/8 11:34:08", 
            "Adder": "wang1", 
            "Usercode": "495", 
            "projectid": "61", 
            "SafeFee": "40000000.00", 
            "CostType": "1", 
            "QuantityType": "1", 
            "ContractorName": null, 
            "ContractModelName": "固定总价合同", 
            "ProjectName": null, 
            "OrgName": null, 
            "OrgID": null, 
            "Types": null, 
            "ProjectCost": null, 
            "ProjectStarStr": null, 
            "ProjectEndStr": null
        }
    ]
}
```