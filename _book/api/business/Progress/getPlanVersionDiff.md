## 查询计划版本对比

> 用于查询计划版本对比

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/getPlanVersionDiff`

### 2. 请求参数

body:

| **参数**                | **数据类型** |  是否必须  | 描述     |
| ------------------------- | :--------: | :--: | ------------------------------------------------------------ |
| **ProjectId** | **String** |  Y   | 项目ID(审核人)                                               |
| **userId** | String | Y | 用户ID |
| **newVersion** | String | Y | 新的计划版本号 |
| **oldVersion** | String | Y | 旧的计划版本号 |
|  |  |  |  |

示例:

``` json
{
  "ProjectId": "",
  "userId": "string",
  "newVersion": "string",
  "oldVersion":""
}
```
### 3. 返回参数

| 字段            | 字段类型 | 字段说明                                                     |
| --------------- | :------: | ------------------------------------------------------------ |
| **Code**        |  string  | 0：成功 ；其他：失败                                         |
| **CodeMsg**     |  String  | 失败时原因信息                                               |
| **newPlan**     |  Object  | 新版计划任务                                                 |
| **oldPlan**     |  Object  | 旧版计划任务                                                 |
| **dayTimeDiff** |  String  | 工期差异 >0工期延长 <0工期提前 =0工期不变（新版本工期-旧版本工期） |
| **taskName**    |  String  | 计划名称                                                     |
| **taskId**      |  String  | 计划task ID                                                  |
| **dayTime**     |  String  | 工期                                                         |
| **startTime**   |  String  | 开始时间                                                     |
| **endTime**     |  String  | 截止时间                                                     |
| **workerNum**   |  String  | 人员数量                                                     |

> `newPlan`和`oldPlan`均不为空（null）  ---- 计划变更，差异
>
> `newPlan`不为空（null），`oldPlan` 为空（null）  ---- 新增计划
>
> `oldPlan` 不为空（null），`newPlan`为空（null）  ---- 删除计划



返回示例：

```json
{
    "Code": 0, 
    "CodeMsg": "OK", 
    "Datas": {
        "dayTimeDiff": "", 
        "diffList": [
            {
                "newPlan": {
                    "taskName": "", 
                    "taskId": "", 
                    "dayTime": "", 
                    "startTime": "", 
                    "endTime": "", 
                    "workerNum": ""
                }, 
                "oldPlan": {
                    "taskName": "", 
                    "taskId": "", 
                    "dayTime": "", 
                    "startTime": "", 
                    "endTime": "", 
                    "workerNum": ""
                }
            }
        ]
    }
}
```