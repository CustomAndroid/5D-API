## 进度查询

> 用于进度查询

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/getPlanSchedule`

### 2. 请求参数

body:

| **参数**                | **数据类型** |  是否必须  | 描述     |
| ------------------------- | :--------: | :--: | ------------------------------------------------------------ |
| **ProjectId** | **String** |  Y   | 项目ID(审核人)                                               |
| **userId** | String | Y | 用户ID |
| **year** | String | Y | 年 |
| **quarter** | String | Y | 季度 |
| **month** | String | Y | 月份 |
| **week** | String | Y | 周数 |

示例:

``` json
{
  "ProjectId": "",
  "userId": "string",
  "year":"2018",
  "quarter":"4",
  "month":"12",
  "week":"2"
}
```
### 3. 返回参数

| 字段              | 字段类型 | 字段说明             |
| ----------------- | :------: | -------------------- |
| **Code**          |  string  | 0：成功 ；其他：失败 |
| **CodeMsg**       |  String  | 失败时原因信息       |
| **taskName**      |  String  | 计划名称             |
| **taskId**        |  String  | taskId               |
| **taskPId**       |  String  | 父级ID               |
| **dayTime**       |  String  | 工期                 |
| **taskPro**       |  String  | 完成百分比           |
| **startTime**     |  String  | 计划开始时间         |
| **endTime**       |  String  | 计划结束时间         |
| **startTimeReal** |  String  | 实际开始时间         |
| **endTimeReal**   |  String  | 实际截止时间         |
| **unit**          |  String  | 施工单位             |
| **workerNum**     |  String  | 人员数量             |
| **equipmentNote** |  String  | 设备说明             |
| **materialNote**  |  String  | 材料说明             |
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
            "taskPId":"",
            "dayTime": "", 
            "taskPro": "", 
            "startTime": "", 
            "endTime": "", 
            "startTimeReal": "", 
            "endTimeReal": "", 
            "unit": "", 
            "workerNum": "", 
            "equipmentNote": "", 
            "materialNote": "", 
            "technology": ""
        }
    ]
}
```