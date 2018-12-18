## 提交施工进度填报

> 用于提交施工进度填报，仅施工人员可填报

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/setPlanSubmitHistory `

### 2. 请求参数

body:

| **参数**                | **数据类型** |  是否必须  | 描述     |
| ------------------------- | :--------: | :--: | ------------------------------------------------------------ |
| **ProjectId** | **String** |  Y   | 项目ID(审核人)                                               |
| **userId** | String | Y | 用户ID |
| **userName** | String | Y | 用户名字 |
| **sendTo** | String | Y | 发送人 |
| **copyTo** | String | N | 抄送人 |
| **localId** | String | N | android上这个字段是个临时ID，用于区分提交那条日志，不入库，提交成功原样返回 |
| **PlanType** | String | Y | 计划类型 4月计划 5旬计划 6周计划 7日计划 |
| **planId** | String |  |  |
| **title** | String | Y | 标题 |
| **startTime** | String | Y | 实际开工时间 |
| **endTime** | String | Y | 实际完成时间 |
| **completePer** | String | Y | 完成比率 |
| **stopWorkingCase** | String | Y/N | 阻工原因，实际开工时间晚于计划开工时间必填 |
| **delayCase** | String | Y/N | 延期原因，实际完工时间晚于计划完工时间 |
| **remark** | String | N | 备注 |
| **modelId** | String | N | 模型ID（好像不用传） |
| **componentId** | String | Y | 构件ID，多个`,`间隔 |
| **FileLists** | String | N | 附件，格式与之前附件格式一致 |
| **TaskId** | String | Y | 计划ID |

示例:

``` json
{
  "sendTo": "string",
  "copyTo": "string",
  "userId": "string",
  "localId": "string",
  "PlanType": "string",
  "ProjectId": "string",
  "planId": "string",
  "title": "string",
  "startTime": "string",
  "endTime": "string",
  "completePer": 0,
  "stopWorkingCase": "string",
  "delayCase": "string",
  "remark": "string",
  "modelId": "string",
  "componentId": "string",
  "FileLists": "string",
  "TaskId": "string"
}
```
### 3. 返回参数

| 字段                    | 字段类型 | 字段说明                            |
| ----------------------- | :------: | ----------------------------------- |
| **Code**                |  string  | 0：成功 ；其他：失败                |
| **CodeMsg**             |  String  | 失败时原因信息                      |
| **planSubmitHistoryId** |  String  | 提交后进度填报ID                    |
| **reportTime**          |  String  | 提交时间                            |
| **localId**             |  String  | android上自己定义的临时ID，原样返回 |



返回示例：

```json
{
    "Code": 0, 
    "CodeMsg": "OK", 
    "Datas": null,
    "planSubmitHistoryId":"",
    "reportTime":"",
    "localId":""
}
```