## 获取进度与计划完成比报表数据

> 用于获取进度与计划完成比报表数据

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/GetScheduleCompletionRatio`

### 2. 请求参数

body:

| 字段              | 字段类型 | 必填 | 字段说明               |
| ----------------- | :------: | :--: | ---------------------- |
| **projectId**     |  String  |  Y   | 项目ID                 |
| **userId**        |  String  |  Y   | 用户ID                 |
| **year**          |  String  |  Y   | 年份                   |
| **quarter**       |  String  |  Y   | 季度                   |
| **unit**          |  String  |  N   | 施工单位               |
| **UserType**      |  String  |  Y   | 用户类型               |
| **vParentTaskID** |  String  |  N   | 父节点ID（根节点传空） |

示例:

```json
{
  "userId": "496",
  "projectId": "61",
  "year": "2018",
  "quarter": "1",
  "unit": "0",
  "UserType": "2",
  "vParentTaskID": ""
}
```

### 3. 返回参数

| 字段           | 字段类型 | 字段说明             |
| -------------- | :------: | -------------------- |
| **Code**       |  string  | 0：成功 ；其他：失败 |
| **CodeMsg**    |  String  | 失败时原因信息       |
| **TaskName**   |  String  | 任务名称             |
| **TaskDeys**   |  String  | 工期                 |
| **PStartDate** |  String  | 计划开始时间         |
| **PEndDate**   |  String  | 计划截止时间         |
| **OrgName**    |  String  | 施工单位             |
| **RStartDate** |  String  | 实际开始时间         |
| **REndDate**   |  String  | 实际截止时间         |
| **TaskPro**    |  String  | 完成百分比           |
| **state**      |  String  | 完成状态             |

返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": [
    {
      "VisId": null,
      "TaskId": "d2a301c9-93c9-477f-bc9b-bc878e1a67a5",
      "TaskName": "马岭河大桥",
      "GuId": "",
      "ProjectId": "61",
      "Unit": null,
      "UnitName": null,
      "TaskDeys": "1826",
      "UserNumber": "0",
      "EquipmentShow": "",
      "MaterialShow": "",
      "Technology": "",
      "TaskType": "0",
      "ParentId": "",
      "PStartDate": "2017/9/1 0:00:00",
      "PEndDate": "2022/9/1 0:00:00",
      "VersionCode": null,
      "EditUser": null,
      "EditDate": null,
      "Note": null,
      "TaskStatus": null,
      "RStartDate": "2017/9/1 0:00:00",
      "REndDate": "2018/9/19 0:00:00",
      "PStatus": null,
      "TaskPro": "21.91",
      "TaskLevel": "0",
      "TaskSource": null,
      "SortOrder": null,
      "MileageID": null,
      "Typestring": null,
      "OrgName": "中铁十二局第二公司,中铁十二局第四公司",
      "state": "closed"
    }
  ]
}
```