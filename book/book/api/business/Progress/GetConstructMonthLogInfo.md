## 查询施工日志详情

> 用于查询施工日志详情,已填报的返回填报的内容，未填报的返回需要填报的字段为空，但会返回计划内施工部位列表用于填报提交，计划内施工部位不可删除，自行新增的施工部位可删除。

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/GetConstructMonthLogInfo `

### 2. 请求参数

body:

| **参数**            | **数据类型** | 是否必须 | 描述                 |
| ------------------- | :----------: | :------: | -------------------- |
| **userid**          |  **String**  |    Y     | 用户ID（填报人ID）   |
| **projectid**       |  **String**  |    Y     | 项目ID(审核人)       |
| **ConstructUnitId** |  **String**  |    Y     | 施工单位ID           |
| **checkDate**       |  **String**  |    Y     | 查询日期  yyyy-MM-dd |
| **UserType**        |  **String**  |    Y     | 用户类型             |

示例:

``` json
{
  "userid": "496",
  "projectid": "61",
  "ConstructUnitId": "418",
  "checkDate": "2018-09-18",
  "UserType": "2"
}
```
### 3. 返回参数

| 字段                                   | 字段类型 | 字段说明                                                     |
| -------------------------------------- | :------: | ------------------------------------------------------------ |
| **Code**                               |  string  | 0：成功 ；其他：失败                                         |
| **CodeMsg**                            |  String  | 失败时原因信息                                               |
| **R_Construction_logModel**            |  Object  | 填报表单数据（未提交为null）                                 |
| **R_Construction_logDetailsModelList** |  Array   | 施工部位列表（未提交返回计划内施工部位，已填报返回计划内和自行新增的施工部位） |
| **R_Construction_logFileModelList**    |  Array   | 附件列表                                                     |
| **IsCanEdit**                          | Boolean  | 是否可编辑（只可编辑当天的）                                 |
| **PlanTaskList**                       |  Array   | 未填报日志时做查询施工部位列表用，已填报时为null             |

`R_Construction_logModel`字段说明：

| 字段                 | 字段类型 | 字段说明                                                     |
| -------------------- | :------: | ------------------------------------------------------------ |
| **Lid**              |  String  | 日志ID                                                       |
| **Projectid**        |  String  | 项目ID                                                       |
| **ConstructionUnit** |  String  | 施工单位ID                                                   |
| **rq**               |  String  | 施工日期                                                     |
| **UserName**         |  String  | 填报人                                                       |
| **Postid**           |  String  | 施工专业ID（查询[getBaseData](../../project/getBaseData.md) `ConstructionMajor`类型） |
| **weatherID**        |  String  | 天气ID（查询[getBaseData](../../project/getBaseData.md) `Weather`类型） |
| **equipmentNum**     |  String  | 施工机具                                                     |
| **UserNum**          |  String  | 施工总人数                                                   |
| **Situation**        |  String  | 施工情况                                                     |
| **equipmentShwo**    |  String  | 设备使用情况                                                 |
| **SituationShow**    |  String  | 施工总结评估                                                 |
| **problem**          |  String  | 施工存在问题                                                 |
| **SafetyShow**       |  String  | 安全质量情况                                                 |
| **Adder**            |  String  | 提报人                                                       |
| **AddDate**          |  String  | 施工日期提报日期                                             |

`R_Construction_logDetailsModelList`字段说明：

| 字段                | 字段类型 | 字段说明                 |
| ------------------- | :------: | ------------------------ |
| **id**              |  String  | ID                       |
| **Lid**             |  String  | 对应施工日志Id           |
| **TaskID**          |  String  | 任务ID                   |
| **site**            |  String  | 施工部位                 |
| **PStartDate**      |  String  | 计划开始时间             |
| **PEndDate**        |  String  | 计划截止时间             |
| **PUserNum**        |  String  | 计划人数                 |
| **PEquipMent**      |  String  | 计划设备                 |
| **RUserNum**        |  String  | 实际人数                 |
| **REquipMent**      |  String  | 实际设备                 |
| **CompletePercent** |  String  | 完成百分比               |
| **Type**            |  String  | 类型 1计划内 2计划外     |
| **IsDelete**        | Boolean  | 是否可删除，计划外可删除 |

**`PlanTaskList`**字段：

| 字段              | 字段类型 | 字段说明             |
| ----------------- | :------: | -------------------- |
| **TaskId**        |  String  | 任务ID               |
| **TaskName**      |  String  | 施工部位             |
| **GuId**          |  String  | 相关构件ID           |
| **ProjectId**     |  String  | 项目ID               |
| **TaskDeys**      |  String  | 工期                 |
| **UserNumber**    |  String  | 计划人数             |
| **EquipmentShow** |  String  | 计划设备             |
| **PStartDate**    |  String  | 计划开始时间         |
| **PEndDate**      |  String  | 计划截止时间         |
| **TaskPro**       |  String  | 进度（填报时可修改） |
| **OrgName**       |  String  | 相关施工单位         |

返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": {
    "R_Construction_logModel": {
      "Lid": "190",
      "Projectid": "61",
      "ConstructionUnit": "418",
      "rq": "2018/9/18 0:00:00",
      "UserName": "wang2",
      "Postid": "1",
      "weatherID": "3",
      "equipmentNum": "5",
      "UserNum": "44",
      "Situation": "挖土方100x325按计划完成",
      "equipmentShwo": "挖掘机 x 1",
      "SituationShow": "分项工程质量验收等级评定为合格",
      "problem": "无",
      "SafetyShow": "无",
      "Adder": "wang2",
      "AddDate": "2018/9/19 0:00:00",
      "PostName": null,
      "WeatherName": null
    },
    "R_Construction_logFileModelList": null,
    "R_Construction_logDetailsModelList": [
      {
        "id": "416",
        "Lid": "190",
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
    ],
    "PlanTaskList": [
      {
        "VisId": null,
        "TaskId": "b51d7314-68ff-4083-a734-050d4db74475",
        "TaskName": "z16-1#桩基_桩基_桩基",
        "GuId": "599_662037",
        "ProjectId": "61",
        "Unit": null,
        "UnitName": null,
        "TaskDeys": "12",
        "UserNumber": "0",
        "EquipmentShow": "",
        "MaterialShow": "",
        "Technology": "",
        "TaskType": "0",
        "ParentId": "7d4ba867-f445-4d75-8f36-e7db1444ebee",
        "PStartDate": "2018/11/25 0:00:00",
        "PEndDate": "2018/12/7 0:00:00",
        "VersionCode": null,
        "EditUser": null,
        "EditDate": null,
        "Note": null,
        "TaskStatus": null,
        "RStartDate": "2018/12/6 0:00:00",
        "REndDate": "2018/12/6 0:00:00",
        "PStatus": null,
        "TaskPro": "2.00",
        "TaskLevel": "4",
        "TaskSource": null,
        "SortOrder": null,
        "MileageID": null,
        "Typestring": null,
        "OrgName": "中铁十二局第二公司,中铁十二局第四公司",
        "state": "open"
      },
      {
        "VisId": null,
        "TaskId": "fb155485-b7fd-4cbf-a84a-0d742f189c78",
        "TaskName": "z16-2#桩基_桩基_桩基",
        "GuId": "599_662558",
        "ProjectId": "61",
        "Unit": null,
        "UnitName": null,
        "TaskDeys": "12",
        "UserNumber": "0",
        "EquipmentShow": "",
        "MaterialShow": "",
        "Technology": "",
        "TaskType": "0",
        "ParentId": "7d4ba867-f445-4d75-8f36-e7db1444ebee",
        "PStartDate": "2018/12/7 0:00:00",
        "PEndDate": "2018/12/19 0:00:00",
        "VersionCode": null,
        "EditUser": null,
        "EditDate": null,
        "Note": null,
        "TaskStatus": null,
        "RStartDate": "",
        "REndDate": "",
        "PStatus": null,
        "TaskPro": "0.00",
        "TaskLevel": "4",
        "TaskSource": null,
        "SortOrder": null,
        "MileageID": null,
        "Typestring": null,
        "OrgName": "中铁十二局第二公司,中铁十二局第四公司",
        "state": "open"
      }
    ],
    "jsonYMD": null,
    "ConstructionUnitName": null,
    "FilePathAndName": null,
    "LogDetails": null,
    "userType": null,
    "IsCanEdit": false
  }
}
```