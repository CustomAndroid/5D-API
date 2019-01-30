## 计划审核列表

> 用于获取施工计划审核列表

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/getPlanAuditList`

### 2. 请求参数

body:

| **参数**                | **数据类型** |  是否必须  | 描述     |
| ------------------------- | :--------: | :--: | ------------------------------------------------------------ |
| **ProjectId** | **String** |  Y   | 项目ID(审核人)                                               |
| **userId** | String | Y | 用户ID |
| **startTime** | String | Y | 开始时间 |
| **endTime** | String | Y | 截止时间 |
| **status** | String | Y | 状态 |
| **keyWord** | String | Y | 关键字 |

示例:

``` json
{
  "ProjectId": "",
  "userId": "string",
  "startTime": "string",
  "endTime": "string",
  "status": "string",
  "keyWord": "string"
}
```
### 3. 返回参数

| 字段            | 字段类型 | 字段说明                              |
| --------------- | :------: | ------------------------------------- |
| **Code**        |  string  | 0：成功 ；其他：失败                  |
| **CodeMsg**     |  String  | 失败时原因信息                        |
| **id**          |  String  | ID                                    |
| **version**     |  String  | 版本号                                |
| **title**       |  String  | 标题                                  |
| **reason**      |  String  | 变更原因                              |
| **Applicant**   |  String  | 申请人                                |
| **addTime**     |  String  | 申请时间                              |
| **status**      |  String  | 状态                                  |
| **audit**       |  String  | 审核权限 0仅浏览 1可审核 2可反馈      |
| **auditStatus** |  String  | 审核状态：1未处理  2正在处理  3已处理 |
| **flows**       |  Array   | 审核流程                              |
| **processor**   |  String  | 审核人                                |
| **addTime**     |  String  | 审核时间                              |
| **ideas**       |  String  | 意见                                  |
| **result**      |  String  | 处理结果                              |

返回示例：

```json
{
    "Code": 0, 
    "CodeMsg": "OK", 
    "Datas": [
        {
            "id": "", 
            "version": "", 
            "title": "", 
            "reason": "", 
            "Applicant": "", 
            "addTime": "", 
            "status": "", 
            "audit": "", 
            "auditStatus": "",
            "flows":[{
                "processor":"",
                "addTime":"",
                "ideas":"",
                "result":""
            }]
        }
    ]
}
```