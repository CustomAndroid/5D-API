## 获取进度沙盘-形象进度

> 获取形象进度

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/getGraphicProgress`

### 2. 请求参数

body:

| 字段                 | 字段类型 | 必填 | 字段说明 |
| -------------------- | :------: | :--: | -------- |
| **userId**           |  String  |  Y   | 用户ID   |
| **constructionUnit** |  String  |  N   | 施工单位 |
| **modelId**          |  String  |  N   | 模型ID   |

传入参数 constructionUnit（施工单位）与modelId（模型ID）二选一,另外一个则传空。

示例:

```json
{
  "userId": "496",
  "constructionUnit":"418",
  "modelId":""
}
```

### 3. 返回参数

| 字段                   | 字段类型 | 字段说明                                                     |
| ---------------------- | :------: | ------------------------------------------------------------ |
| **guids**             |  string  | 相关构件ID                                                |
| **taskId** | string | 任务ID |
| **taskPId** | string | 父ID |
| **taskName** | string | 任务名称 |
| **completeRate** | string | 完成百分比 |
| **taskDays** | string | 工期 |
| **startTimePlan** | string | 计划开始时间 |
| **endTimePlan** | string | 计划截止时间 |
| **startTimeReal** | string | 实际开始时间 |
| **lastTime** | string | 最新填报时间 |


返回示例：

```json
{
    "Code": 0, 
    "CodeMsg": "ok", 
    "Datas": [
        {
            "guids": "", 
            "taskId": "", 
            "taskPId": "", 
            "taskName": "", 
            "completeRate": "", 
            "taskDays": "", 
            "startTimePlan": "", 
            "endTimePlan": "", 
            "startTimeReal": "", 
            "lastTime": ""
        }
    ]
}
```
