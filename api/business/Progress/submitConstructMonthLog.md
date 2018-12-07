## 施工日志提交

> 用于提交施工日志

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/submitConstructMonthLog `

### 2. 请求参数

body:

| **参数**                | **数据类型** |  是否必须  | 描述     |
| ------------------------- | ---------- | :--: | ------------------------------------------------------------ |
| **userId**                | **String** |  Y   | 用户ID（填报人ID）                                           |
| **projectId**             | **String** |  Y   | 项目ID(审核人)                                               |
| **R_Construction_logModel** |  |  | 日志详情内容 |
| **ConstructUnitId**       | **String** |  Y   | 施工单位ID                                                   |
| **checkDate**             | **String** |  Y   | 查询日期（yyyy-MM-dd）                                       |
| **ConstructionSpecialty** | **String** |  Y   | 施工专业                                                     |
| **weather**               | **String** |  Y   | 天气                                                         |
| **equipmentNum**          | **String** |  Y   | 施工机具                                                     |
| **UserNum**               | **String** |  Y   | 施工总人数                                                   |
| **SituationShow**         | **String** |  Y   | 施工情况                                                     |
| **equipmentShwo**         | **String** |  Y   | 设备使用情况                                                 |
| **Situation**             | **String** |  Y   | 施工总结评估                                                 |
| **problem**               | **String** |  N   | 施工存在问题                                                 |
| **SafetyShow**            | **String** |  N   | 安全质量情况                                                 |
| **fileList**              | **String** |  N   | 附件(文件名:描述,文件名:描述)                                |
| **logDetailsModelList**   | Array |  Y   | 施工部位列表 |
| **CompletePercent** |  |  | 完成百分比 |
| **IsDelete** |  |  | true 自定义任务，false计划任务 |
| **PEndDate** |  |  | 计划截止时间 |
| **PStartDate** |  |  | 计划开始时间 |
| **PUserNum** |  |  | 计划人数 |
| **PEquipMent** |  |  | 计划设备 |
| **REquipMent** |  |  | 实际设备 |
| **RUserNum** |  |  | 实际人数 |
| **TaskID** |  |  | 计划ID，自定义任务没有 |
| **Type** |  |  | 1计划内任务，2自定义任务 |
| **id** |  |  | 自定义任务id为 `tmp_`开头,提交后服务器处理数据时id自增 |
| **site** |  |  | 施工部位 |
| **R_Construction_logFileModelList** | Array |  | 附件列表 |
| **filepath** | String |  | 上传文件路径 |
| **filetype** | String |  | 文件类型，后缀名 |
| **filename** | String |  | 文件名，描述 |

示例:

``` json
{
    "IsCanEdit": true, 
    "R_Construction_logDetailsModelList": [
        {
            "CompletePercent": "12.00", 
            "IsDelete": false, 
            "PEndDate": "2018/12/7", 
            "PEquipMent": "0", 
            "PStartDate": "2018/11/25", 
            "PUserNum": "0", 
            "REquipMent": "9", 
            "RUserNum": "12", 
            "TaskID": "b51d7314-68ff-4083-a734-050d4db74475", 
            "Type": "1", 
            "id": "tmp_1544179256381", 
            "site": "z16-1#桩基_桩基_桩基"
        }, 
        {
            "CompletePercent": "10.00", 
            "IsDelete": false, 
            "PEndDate": "2018/12/19", 
            "PEquipMent": "0", 
            "PStartDate": "2018/12/7", 
            "PUserNum": "0", 
            "REquipMent": "8", 
            "RUserNum": "13", 
            "TaskID": "fb155485-b7fd-4cbf-a84a-0d742f189c78", 
            "Type": "1", 
            "id": "tmp_1544179256381", 
            "site": "z16-2#桩基_桩基_桩基"
        }, 
        {
            "CompletePercent": "10", 
            "IsDelete": true, 
            "PEndDate": "2018-12-07", 
            "PEquipMent": "9", 
            "PStartDate": "2018-12-01", 
            "PUserNum": "12", 
            "REquipMent": "9", 
            "RUserNum": "11", 
            "id": "tmp_1544179289195", 
            "site": "自定义任务"
        }
    ], 
    "R_Construction_logFileModelList": [
        {
            "filename": "图片1", 
            "filepath": "/uploadFile/attachment/EF_20181207_184334614.png", 
            "filetype": ".png"
        }, 
        {
            "filename": "", 
            "filepath": "/uploadFile/attachment/EF_20181207_184334613.png", 
            "filetype": ".png"
        }, 
        {
            "filename": "附件3", 
            "filepath": "/uploadFile/attachment/EF_20181207_184334613.png", 
            "filetype": ".png"
        }
    ], 
    "R_Construction_logModel": {
        "AddDate": "2018-12-07", 
        "Adder": "496", 
        "ConstructionUnit": "418", 
        "PostName": "土建", 
        "Postid": "1", 
        "Projectid": "61", 
        "SafetyShow": "安全质量问题", 
        "Situation": "施工情况", 
        "SituationShow": "施工工作总结", 
        "UserName": "wang2", 
        "UserNum": "23", 
        "WeatherName": "雪天", 
        "equipmentNum": "15", 
        "equipmentShwo": "设备使用情况", 
        "problem": "存在问题", 
        "rq": "2018-12-07", 
        "weatherID": "3"
    }
}
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