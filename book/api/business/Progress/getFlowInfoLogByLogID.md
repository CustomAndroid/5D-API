## 根据FlowId 查询施工日志审批流程

> 用于根据FlowId 查询施工日志审批流程

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/getFlowInfoLogByLogID`

### 2. 请求参数

body:

| **参数**                | **数据类型** |  是否必须  | 描述     |
| ------------------------- | :--------: | :--: | ------------------------------------------------------------ |
| **ProjectId** | **String** |  Y   | 项目ID(审核人)                                               |
| **userid** | String | Y | 用户ID |
| **LogID** | String | Y | 进度填报ID |

示例:

``` json
{
  "LogID": "string"
}
```
### 3. 返回参数

| 字段                 | 字段类型 | 字段说明             |
| -------------------- | :------: | -------------------- |
| **Code**             |  string  | 0：成功 ；其他：失败 |
| **CodeMsg**          |  String  | 失败时原因信息       |
| **FlowStepId**       |  String  | 审核流程ID           |
| **idea**             |  String  | 处理意见             |
| **realityRate**      |  String  | 实际完成万分比       |
| **Comment**          |  String  | 处理措施             |
| **AuditingUserName** |  String  | 审核人               |
| **DealDateTime**     |  String  | 审核日期             |



返回示例：

```json
{
    "Code": 0, 
    "CodeMsg": "OK", 
    "Datas": [
        {
            "FlowStepId": "89", 
            "idea": "1", 
            "realityRate": "3.00", 
            "Comment": "qq", 
            "AuditingUserName": "范力卓", 
            "DealDateTime": "2017-12-26"
        }
    ]
}
```