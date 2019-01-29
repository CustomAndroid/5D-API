## 根据ID获取进度填报

> 用于根据ID获取进度填报

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/getPlanLogById`

### 2. 请求参数

body:

| **参数**                | **数据类型** |  是否必须  | 描述     |
| ------------------------- | :--------: | :--: | ------------------------------------------------------------ |
| **ProjectId** | **String** |  Y   | 项目ID(审核人)                                               |
| **userid** | String | Y | 用户ID |
| **vid** | String | Y | （没用） |
| **logId** | String | Y | 进度填报ID |

示例:

``` json
{
  "vid": "string",
  "userId": "string",
  "projectId": "string",
  "logId": "string"
}
```
### 3. 返回参数

| 字段                 | 字段类型 | 字段说明             |
| -------------------- | :------: | -------------------- |
| **Code**             |  string  | 0：成功 ；其他：失败 |
| **CodeMsg**          |  String  | 失败时原因信息       |
| **AutiId**           |  String  | 审核ID？             |
| **NoteID**           |  String  | 进度填报ID           |
| **title**            |  String  | 标题                 |
| **applicant**        |  String  | t提报人              |
| **addTime**          |  String  | t提报时间            |
| **startTime**        |  String  | 开工时间             |
| **endTime**          |  String  | 完工时间             |
| **stopWorkCause**    |  String  | 组工原因             |
| **delayCause**       |  String  | 延期原因             |
| **remark**           |  String  | 备注                 |
| **completionRate**   |  String  | 填报完成百分比       |
| **Files**            |  String  | 附件                 |
| **myJurisdiction**   |  String  | 我的审核权限 0可审核 |
| **auditingList**     |  Array   | 历史审核列表         |
| **FlowStepId**       |  String  | 审核流程ID           |
| **idea**             |  String  | 处理意见             |
| **realityRate**      |  String  | 实际完成万分比       |
| **Comment**          |  String  | 处理措施             |
| **AuditingUserName** |  String  | 审核人               |
| **DealDateTime**     |  String  | 审核日期             |
| **guid**             |  String  | 构件ID               |



返回示例：

```json
{
    "Code": 0, 
    "CodeMsg": "OK", 
    "Datas": [
        {
            "AutiId": "7faa4331-9477-4c03-862b-93bd80bc1935", 
            "NoteID": "fac804a5-6617-4c94-b0a3-fccb566ee460", 
            "title": "[施工日志填报申请]", 
            "applicant": "仇轩", 
            "addTime": "2017-12-26", 
            "applicationAgency": "", 
            "startTime": "2017-12-19", 
            "endTime": "2017-12-26", 
            "stopWorkCause": "zg", 
            "delayCause": "y", 
            "remark": "q", 
            "completionRate": "3.00", 
            "enclosureFiles": null, 
            "Files": "", 
            "myJurisdiction": "0", 
            "auditingList": [
                {
                    "FlowStepId": "89", 
                    "idea": "1", 
                    "realityRate": "3.00", 
                    "Comment": "qq", 
                    "AuditingUserName": "范力卓", 
                    "DealDateTime": "2017-12-26"
                }
            ], 
            "guid": ""
        }
    ]
}
```