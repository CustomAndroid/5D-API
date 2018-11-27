## 施工日志提交

> 用于提交施工日志

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/submitConstructMonthLog `

### 2. 请求参数

body:
| **userId**                | **String** | Y    | 用户ID（填报人ID）                                           |
| ------------------------- | ---------- | ---- | ------------------------------------------------------------ |
| **projectId**             | **String** | Y    | 项目ID(审核人)                                               |
| **ConstructUnitId**       | **String** | Y    | 施工单位ID                                                   |
| **checkDate**             | **String** | Y    | 查询日期（yyyy-MM-dd）                                       |
| **ConstructionSpecialty** | **String** | Y    | 施工专业                                                     |
| **weather**               | **String** | Y    | 天气                                                         |
| **equipmentNum**          | **String** | Y    | 施工机具                                                     |
| **UserNum**               | **String** | Y    | 施工总人数                                                   |
| **SituationShow**         | **String** | N    | 施工情况                                                     |
| **equipmentShwo**         | **String** | N    | 设备使用情况                                                 |
| **Situation**             | **String** | N    | 施工总结评估                                                 |
| **problem**               | **String** | N    | 施工存在问题                                                 |
| **SafetyShow**            | **String** | N    | 安全质量情况                                                 |
| **fileList**              | **String** | N    | 附件(文件名:描述,文件名:描述)                                |
| **logDetailsModelList**   | **String** | Y    | 施工部位列表(json字符串),包括(计划内、计划外)： 施工部位 计划时间段 计划人数 计划设备 实际人数 设备数量 累计完成百分比 |

示例:

``` json
{
    "userId": "", 
    "projectId": "", 
    "ConstructUnitId": "", 
    "checkDate": "", 
    "ConstructionSpecialty": "", 
    "weather": "", 
    "equipmentNum": "", 
    "UserNum": "", 
    "SituationShow": "", 
    "equipmentShwo": "", 
    "Situation": "", 
    "problem": "", 
    "SafetyShow": "", 
    "fileList": "", 
    "logDetailsModelList": "[/**参考下面格式**/ ]"
}
```
logDetailsModelList 字段格式如下
``` json
[
    {
        "id": "415", //新建的此项为tmp_ 开头的临时ID
        "Lid": "189", //新建的此项为空 
        "TaskID": "c34dddbf-0f45-4d7a-b986-f9046e879f8a", //新建的此项为空 
        "site": "Y16承台_Z16承台_Z16承台", 
        "PStartDate": "2018/8/17 0:00:00", 
        "PEndDate": "2018/9/11 0:00:00", 
        "PUserNum": "0", 
        "PEquipMent": "", 
        "RUserNum": "103", 
        "REquipMent": "12", 
        "CompletePercent": "100.00", 
        "Type": "1", 
        "IsDelete": false //新建的此项为true
    }
]
```
### 3. 返回参数

| 字段        | 字段类型 | 字段说明               |
| ----------- | :------: | ---------------------- |
| **Code**    |  string  | 0：成功 ；其他：失败   |
| **CodeMsg** |  String  | 失败时原因信息         |

返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": null
}
```