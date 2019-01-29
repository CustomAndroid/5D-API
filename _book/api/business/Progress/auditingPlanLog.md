## 施工进度填报审核

> 用于施工进度填报审核,

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/auditingPlanLog`

### 2. 请求参数

body:

| **参数**                | **数据类型** |  是否必须  | 描述     |
| ------------------------- | :--------: | :--: | ------------------------------------------------------------ |
| **ProjectId** | **String** |  Y   | 项目ID(审核人)                                               |
| **userid** | String | Y | 用户ID |
| **logId** | String | Y | 审核第几步ID |
| **FlowId** |  |  | 流程I的（历史审核列表最新一条） |
| **idea** |  |  | 审核意见 1同意 2不同意 |
| **realityRate** |  |  | 实际完成百分比 |
| **Comment** |  |  | 措施 |
| **sendTo** |  |  | 发送人 |
| **copyTo** |  |  | 抄送人 |
| **type** |  |  | 1代表审核结束；0:代表审核并发送下一人 |
| **HOrgID** |  |  | 当前登录人所在组织ID |
| **RealComPer** |  |  | 同`realityRate` |
| **UserHOrgName** |  |  | 组织名 |

示例:

``` json
{
  "Vid": 0,
  "userId": "string",
  "FlowId": "string",
  "logId": "string",
  "idea": "string",
  "realityRate": "string",
  "Comment": "string",
  "sendTo": "string",
  "copyTo": "string",
  "type": "string",
  "HOrgID": "string",
  "RealComPer": "string",
  "UserHOrgName": "string"
}
```
### 3. 返回参数

| 字段        | 字段类型 | 字段说明             |
| ----------- | :------: | -------------------- |
| **Code**    |  string  | 0：成功 ；其他：失败 |
| **CodeMsg** |  String  | 失败时原因信息       |



返回示例：

```json
{
    "Code": 0, 
    "CodeMsg": "OK", 
    "Datas":null
}
```