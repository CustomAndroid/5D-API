## 获取/更新项目施工计划及版本

> 用于获取/更新项目施工计划及版本

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/getPlanAndVersion `

### 2. 请求参数

body:

| **参数**                | **数据类型** |  是否必须  | 描述     |
| ------------------------- | :--------: | :--: | ------------------------------------------------------------ |
| **Projectid** | **String** |  Y   | 项目ID(审核人)                                               |

示例:

``` json
{
  "Projectid": "61"
}
```
### 3. 返回参数

| 字段              | 字段类型 | 字段说明                                                     |
| ----------------- | :------: | ------------------------------------------------------------ |
| **Code**          |  string  | 0：成功 ；其他：失败                                         |
| **CodeMsg**       |  String  | 失败时原因信息                                               |
| **TaskID**        |          | 计划任务ID（可查询模型ID和名称用于加载模型，模型加载完调用引擎api`SetActorColor(GUIDS,RED,GREEN,BLUE)`设置构件颜色以标识，或调用二次开发api[`setActorsColor(guids, r, g, b)`](https://github.com/Sogrey/3DEngineToolsBox/blob/master/3DEngineToolsBoxHandbook.md#setActorsColor)设置）,其中`GUID`就是返回中的GUID↓ |
| **TaskName**      |          | 名称                                                         |
| **ParentID**      |          | 父节点ID                                                     |
| **GuId**          |          | 该计划关联的构件ID（父节点为空）                             |
| **PStartDate**    |          | 计划开始时间                                                 |
| **PEndDate**      |          | 计划截止时间                                                 |
| **RStartDate**    |          | 实际开始时间                                                 |
| **REndDate**      |          | 实际截止时间                                                 |
| **TaskPro**       |          | 完成百分比                                                   |
| **UserNumber**    |          | 人数                                                         |
| **EquipmentShow** |          | 设备                                                         |
| **MaterialShow**  |          | 材料                                                         |
| **TaskDeys**      |          | 工期                                                         |
| **OrgName**       |          | 参建施工单位                                                 |



返回示例：

```json
{
    "Code": 0, 
    "CodeMsg": "OK", 
    "Datas": [
        {
            "TaskID": "d2a301c9-93c9-477f-bc9b-bc878e1a67a5", 
            "TaskName": "马岭河大桥", 
            "ParentID": null, 
            "GuId": "", 
            "PStartDate": "2017/9/1 0:00:00", 
            "PEndDate": "2022/9/1 0:00:00", 
            "RStartDate": "2017/9/1 0:00:00", 
            "REndDate": "2018/9/19 0:00:00", 
            "TaskPro": 21.91, 
            "UserNumber": 502, 
            "EquipmentShow": "", 
            "MaterialShow": "", 
            "Technology": "", 
            "TypeInt": 0, 
            "TaskType": 0, 
            "TaskDeys": 1826, 
            "OrgName": "中铁十二局第二公司,中铁十二局第四公司", 
            "children": null, 
            "state": null, 
            "ModelName": ""
        }, 
        {
            "TaskID": "e2a87700-0212-41f9-a140-4beeab00c0b0", 
            "TaskName": "主桥", 
            "ParentID": "d2a301c9-93c9-477f-bc9b-bc878e1a67a5", 
            "GuId": "", 
            "PStartDate": "2017/9/1 0:00:00", 
            "PEndDate": "2020/3/2 0:00:00", 
            "RStartDate": "2017/9/1 0:00:00", 
            "REndDate": "2018/9/19 0:00:00", 
            "TaskPro": 43.81, 
            "UserNumber": 0, 
            "EquipmentShow": "", 
            "MaterialShow": "", 
            "Technology": "", 
            "TypeInt": 0, 
            "TaskType": 0, 
            "TaskDeys": 913, 
            "OrgName": "中铁十二局第二公司,中铁十二局第四公司", 
            "children": null, 
            "state": null, 
            "ModelName": ""
        }, 
        {
            "TaskID": "f1f8e1af-d906-4ccb-8b04-1745600d9702", 
            "TaskName": "标高 12", 
            "ParentID": "e2a87700-0212-41f9-a140-4beeab00c0b0", 
            "GuId": "", 
            "PStartDate": "2018/10/9 0:00:00", 
            "PEndDate": "2018/11/29 0:00:00", 
            "RStartDate": "", 
            "REndDate": "", 
            "TaskPro": 0, 
            "UserNumber": 0, 
            "EquipmentShow": "", 
            "MaterialShow": "", 
            "Technology": "", 
            "TypeInt": 0, 
            "TaskType": 0, 
            "TaskDeys": 51, 
            "OrgName": "中铁十二局第二公司,中铁十二局第四公司", 
            "children": null, 
            "state": null, 
            "ModelName": ""
        }, 
        {
            "TaskID": "8c3af9a7-c080-4f74-a601-3ecc677f525c", 
            "TaskName": "标高 13", 
            "ParentID": "e2a87700-0212-41f9-a140-4beeab00c0b0", 
            "GuId": "", 
            "PStartDate": "2018/11/29 0:00:00", 
            "PEndDate": "2019/1/19 0:00:00", 
            "RStartDate": "", 
            "REndDate": "", 
            "TaskPro": 0, 
            "UserNumber": 0, 
            "EquipmentShow": "", 
            "MaterialShow": "", 
            "Technology": "", 
            "TypeInt": 0, 
            "TaskType": 0, 
            "TaskDeys": 51, 
            "OrgName": "中铁十二局第二公司,中铁十二局第四公司", 
            "children": null, 
            "state": null, 
            "ModelName": ""
        }, 
        {
            "TaskID": "6e465053-478e-4946-aa34-b9d921c79452", 
            "TaskName": "常规模型", 
            "ParentID": "f1f8e1af-d906-4ccb-8b04-1745600d9702", 
            "GuId": "", 
            "PStartDate": "2018/10/9 0:00:00", 
            "PEndDate": "2018/11/29 0:00:00", 
            "RStartDate": "", 
            "REndDate": "", 
            "TaskPro": 0, 
            "UserNumber": 0, 
            "EquipmentShow": "", 
            "MaterialShow": "", 
            "Technology": "", 
            "TypeInt": 0, 
            "TaskType": 0, 
            "TaskDeys": 51, 
            "OrgName": "中铁十二局第二公司,中铁十二局第四公司", 
            "children": null, 
            "state": null, 
            "ModelName": ""
        }, 
        {
            "TaskID": "7d4ba867-f445-4d75-8f36-e7db1444ebee", 
            "TaskName": "常规模型", 
            "ParentID": "8c3af9a7-c080-4f74-a601-3ecc677f525c", 
            "GuId": "", 
            "PStartDate": "2018/11/29 0:00:00", 
            "PEndDate": "2019/1/19 0:00:00", 
            "RStartDate": "", 
            "REndDate": "", 
            "TaskPro": 0, 
            "UserNumber": 0, 
            "EquipmentShow": "", 
            "MaterialShow": "", 
            "Technology": "", 
            "TypeInt": 0, 
            "TaskType": 0, 
            "TaskDeys": 51, 
            "OrgName": "中铁十二局第二公司,中铁十二局第四公司", 
            "children": null, 
            "state": null, 
            "ModelName": ""
        }, 
        {
            "TaskID": "c7702e97-fd1d-4c8d-a2c5-994ef7c986a9", 
            "TaskName": "z18-1#桩基_桩基_桩基", 
            "ParentID": "6e465053-478e-4946-aa34-b9d921c79452", 
            "GuId": "599_599746", 
            "PStartDate": "2018/11/2 0:00:00", 
            "PEndDate": "2018/11/8 0:00:00", 
            "RStartDate": "", 
            "REndDate": "", 
            "TaskPro": 0, 
            "UserNumber": 0, 
            "EquipmentShow": "", 
            "MaterialShow": "", 
            "Technology": "", 
            "TypeInt": 0, 
            "TaskType": 0, 
            "TaskDeys": 6, 
            "OrgName": "中铁十二局第二公司,中铁十二局第四公司", 
            "children": null, 
            "state": null, 
            "ModelName": ""
        }, 
        {
            "TaskID": "1f84b5d1-0ee7-4b50-a5f8-bbceef789005", 
            "TaskName": "z18-2#桩基_桩基_桩基", 
            "ParentID": "6e465053-478e-4946-aa34-b9d921c79452", 
            "GuId": "599_600274", 
            "PStartDate": "2018/11/8 0:00:00", 
            "PEndDate": "2018/11/15 0:00:00", 
            "RStartDate": "", 
            "REndDate": "", 
            "TaskPro": 0, 
            "UserNumber": 0, 
            "EquipmentShow": "", 
            "MaterialShow": "", 
            "Technology": "", 
            "TypeInt": 0, 
            "TaskType": 0, 
            "TaskDeys": 7, 
            "OrgName": "中铁十二局第二公司,中铁十二局第四公司", 
            "children": null, 
            "state": null, 
            "ModelName": ""
        }
    ]
}
```