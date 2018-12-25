## 查询关键路径延期预警

> 用于查询关键路径延期预警

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/getDelayWarningList`

### 2. 请求参数

body:

| **参数**                | **数据类型** |  是否必须  | 描述     |
| ------------------------- | :--------: | :--: | ------------------------------------------------------------ |
| **ProjectId** | **String** |  Y   | 项目ID(审核人)                                               |
| **userId** | String | Y | 用户ID |
| **type** | String | Y | 预警类型（0开工延期提醒，1开工延期预警，2完工延期提醒，3完工延期预警） |

示例:

``` json
{
  "ProjectId": "",
  "userId": "string",
  "type":"0"
}
```
### 3. 返回参数

| 字段              | 字段类型 | 字段说明             |
| ----------------- | :------: | -------------------- |
| **Code**          |  string  | 0：成功 ；其他：失败 |
| **CodeMsg**       |  String  | 失败时原因信息       |
| **taskName**      |  String  | 计划名称             |
| **taskId**        |  String  | taskId               |
| **dayTime**       |  String  | 工期                 |
| **taskPro**       |  String  | 完成百分比           |
| **startTime**     |  String  | 计划开始时间         |
| **endTime**       |  String  | 计划结束时间         |
| **startTimeReal** |  String  | 实际开始时间         |
| **lastTime**      |  String  | 最后填报时间         |
| **note**          |  String  | 工程量说明           |
| **technique**     |  String  | 工艺工法             |



返回示例：

```json
{
    "Code": 0, 
    "CodeMsg": "OK", 
    "Datas": [
        {
            "taskName": "", 
            "taskId": "", 
            "dayTime": "", 
            "taskPro": "", 
            "startTime": "", 
            "endTime": "", 
            "startTimeReal": "", 
            "lastTime": "", 
            "note": "", 
            "technique": ""
        }
    ]
}
```