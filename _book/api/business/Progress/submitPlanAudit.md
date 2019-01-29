## 计划审核

> 用于提报计划审核

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/submitPlanAudit`

### 2. 请求参数

body:

| **参数**                | **数据类型** |  是否必须  | 描述     |
| ------------------------- | :--------: | :--: | ------------------------------------------------------------ |
| **ProjectId** | **String** |  Y   | 项目ID(审核人)                                               |
| **userId** | String | Y | 用户ID |
| **planAuditId** | String | Y | 计划审核ID |
| **ideas** | String | Y | 意见 |
| **result** | String | Y | 处理结果 |

示例:

``` json
{
  "ProjectId": "",
  "userId": "string",
  "planAuditId": "string",
  "ideas": "string",
  "result": "string"
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
    "Datas": null
}
```