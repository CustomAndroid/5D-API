## 查询具体日期施工部位列表（施工日志）

> 用于在当天未填写的施工日志时获取这一天施工部位列表用于填报

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/GetconstructionSites `

### 2. 请求参数

body:

| **参数**            | **数据类型** | 是否必须 | 描述                 |
| ------------------- | :----------: | :------: | -------------------- |
| **userid**          |  **String**  |    Y     | 用户ID（填报人ID）   |
| **projectid**       |  **String**  |    Y     | 项目ID(审核人)       |
| **ConstructUnitId** |  **String**  |    Y     | 施工单位ID           |
| **checkDate**       |  **String**  |    Y     | 查询日期  yyyy-MM-dd |

示例:

``` json
{
  "userid": "496",
  "projectid": "61",
  "ConstructUnitId": "418",
  "checkDate": "2018-09-18"
}
```
### 3. 返回参数

| 字段                | 字段类型 | 字段说明                                       |
| ------------------- | :------: | ---------------------------------------------- |
| **Code**            |  string  | 0：成功 ；其他：失败                           |
| **CodeMsg**         |  String  | 失败时原因信息                                 |
| **id**              |  String  | ID                                             |
| **Lid**             |  String  | 对应施工日志Id，未填报日志 Lid 为null 或不返回 |
| **TaskID**          |  String  | 任务ID                                         |
| **site**            |  String  | 施工部位                                       |
| **PStartDate**      |  String  | 计划开始时间                                   |
| **PEndDate**        |  String  | 计划截止时间                                   |
| **PUserNum**        |  String  | 计划人数                                       |
| **PEquipMent**      |  String  | 计划设备                                       |
| **RUserNum**        |  String  | 实际人数                                       |
| **REquipMent**      |  String  | 实际设备                                       |
| **CompletePercent** |  String  | 完成百分比                                     |
| **Type**            |  String  | 类型 1计划内 2计划外                           |
| **IsDelete**        | Boolean  | 是否可删除，计划外可删除                       |


返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": [
      {
        "id": "416",
        "Lid": null,//未填报日志 Lid 为null 或不返回
        "TaskID": "e9d33f81-e94e-4ecf-b4c4-53c2b3127c87",
        "site": "Y21承台_Y21承台_Y21承台",
        "PStartDate": "2018/9/13 0:00:00",
        "PEndDate": "2018/10/9 0:00:00",
        "PUserNum": "0",
        "PEquipMent": "",
        "RUserNum": "103",
        "REquipMent": "12",
        "CompletePercent": "100.00",
        "Type": "1",
        "IsDelete": false
      }
    ]
}
```