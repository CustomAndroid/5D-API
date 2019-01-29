## 根据ID获取进度审核详情

> 用于根据ID获取进度审核详情

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/getProgressVerifyLogById`

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
| **enclosureFiles**   |  String  | 附件                 |
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
            "AutiId": "735", 
            "NoteID": "446", 
            "title": "引桥", 
            "applicant": "王飞", 
            "addTime": "2018/8/22 18:50:37", 
            "applicationAgency": "西安建筑二局三公司", 
            "startTime": "2018/8/2 0:00:00", 
            "endTime": "2018/8/4 0:00:00", 
            "stopWorkCause": "阻工", 
            "delayCause": "", 
            "remark": "备注", 
            "completionRate": "0.00", 
            "enclosureFiles": [ ], 
            "myJurisdiction": null, 
            "guid": null, 
            "auditingList": [
                {
                    "FlowStepId": "0", 
                    "idea": "1", 
                    "realityRate": "0.00", 
                    "Comment": "", 
                    "AuditingUserName": "wyx102", 
                    "DealDateTime": "1990/1/1 0:00:00", 
                    "FlowStepStatus": "1"
                }
            ]
        }
    ]
}
```