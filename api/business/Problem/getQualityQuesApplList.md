## 质量问题审核列表

> 用于获取质量问题审核列表，和 `getQualityQuesList`类似，此接口获取的是需要当前登录人审核/参与审核已审核的问题列表

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/getQualityQuesApplList`

### 2. 请求参数

body:

| 字段          | 字段类型 | 必填 | 字段说明                                                     |
| ------------- | :------: | :--: | ------------------------------------------------------------ |
| **projectId** |  String  |  Y   | 项目ID                                                       |
| **startTime** |  String  |  Y   | 开始时间                                                     |
| **endTime**   |  String  |  Y   | 结束时间                                                     |
| **userId**    |  String  |  N   | 用户ID                                                       |
| **level**     |  String  |  N   | 问题危险登记，[GetBaseData](../../project/getBaseData.md)接口获取类型为`QualityProblemLevel` |
| **status**    |  String  |  N   | 问题状态：1-未处理；2-正在处理；3-已完成                     |
| **keyWord**   |  String  |  N   | 关键字                                                       |
| **pageIndex** |  String  |  Y   | 页码                                                         |
| **pagesize**  |  String  |  Y   | 每页条数                                                     |
| **qid**       |  String  |  N   | 忽略传空                                                     |

示例:

```json
{
  "userId": "496",
  "pageIndex": "1",
  "startTime": "2018-06-30",
  "endTime": "2018-11-30",
  "level": "",
  "status": "",
  "keyWord": "",
  "pagesize": "20",
  "qid": ""
}
```

### 3. 返回参数

| 字段                 | 字段类型 | 字段说明                                                     |
| -------------------- | :------: | ------------------------------------------------------------ |
| **Code**             |  string  | 0：成功 ；其他：失败                                         |
| **CodeMsg**          |  String  | 失败时原因信息                                               |
| **id**               |  String  | 问题ID                                                       |
| **level**            |  String  | 危险等级Id                                                   |
| **levelName**        |  String  | 危险等级名称                                                 |
| **Status**           |  String  | 处理状态                                                     |
| **statusName**       |  String  | 状态名称                                                     |
| **aroseTime**        |  String  | 发现问题时间                                                 |
| **reportTime**       |  String  | 提报时间                                                     |
| **quesType**         |  String  | 问题类型ID                                                   |
| **quesTypeName**     |  String  | 问题类型名称                                                 |
| **guid**             |  String  | 此问题关联的构件ID，多个`;`间隔                              |
| **desc1**            |  String  | 描述                                                         |
| **reportPerson**     |  String  | 提报人ID                                                     |
| **reportPersonName** |  String  | 提报人名称                                                   |
| **enclosureList**    |  String  | 附件，以`附件1:附件1的描述,附件2:附件2的描述`的格式返回，多个附件`,`间隔，附件名与其描述`:`间隔，附件名是相对路径，前面拼接上 [login](../../login/login.md) 中返回的 `WebNetIPAndPort` |
| **myJurisdiction**   |  String  | 我的审核权限，`0`可审核，`1`仅查看                           |
| **isReView**         |  String  | 0审核 1反馈                                                  |
| **LableLocation**    |  String  | 标签三维坐标，调引擎设置标签api                              |
| **ViewPoint**        |  String  | 视点，设置相机三维空间坐标，调引擎设置视点api                |



返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": [
    {
      "id": "119",
      "QTitle": "环境污染问题",
      "level": "1",
      "levelName": "轻微",
      "Status": "3",
      "statusName": "已完成",
      "aroseTime": "2018-09-19",
      "reportTime": "2018/9/19 11:53:00",
      "quesType": "4",
      "quesTypeName": "其他",
      "guid": "",
      "sectionName": "",
      "lineMileage": "",
      "modelType": "",
      "desc1": "<p>问题流程测试</p>",
      "reportPerson": "498",
      "reportPersonName": "wang3",
      "enclosureList": "",
      "myJurisdiction": "1",
      "LableLocation": "",
      "isReView": "0",
      "ViewPoint": ""
    },
    {
      "id": "116",
      "QTitle": "墩柱质量存在问题",
      "level": "1",
      "levelName": "轻微",
      "Status": "3",
      "statusName": "已完成",
      "aroseTime": "2018-09-13",
      "reportTime": "2018/9/13 11:41:00",
      "quesType": "4",
      "quesTypeName": "其他",
      "guid": "600_943714;600_648898;600_943832;600_646800",
      "sectionName": "",
      "lineMileage": "",
      "modelType": "",
      "desc1": "",
      "reportPerson": "496",
      "reportPersonName": "wang2",
      "enclosureList": "",
      "myJurisdiction": "1",
      "LableLocation": ";;74654.98974609375,-162608.02594392287,1810079.4375,0.5242870522863372,0,-0.22015739215810728,-19070.242707817437,-286470.7048776565,1779779.263420249;74654.98974609375,-162608.02594392287,1810079.4375,0.5242870522863372,0,-0.22015739215810728,-13159.692799659177,-280955.08642132586,1785129.8326502228;74654.98974609375,-162608.02594392287,1810079.4375,0.5242870522863372,0,-0.22015739215810728,-9293.623113941765,-289993.9120036639,1780151.6134423825;74654.98974609375,-162608.02594392287,1810079.4375,0.5242870522863372,0,-0.22015739215810728,-12229.136064920167,-287907.3840155277,1778193.397932513;74654.98974609375,-162608.02594392287,1810079.4375,0.5242870522863372,0,-0.22015739215810728,-14967.668541158695,-282787.138241184,1784106.9976517071;74654.98974609375,-162608.02594392287,1810079.4375,0.5242870522863372,0,-0.22015739215810728,-31424.038296353177,-284536.3460023052,1779574.8307700271",
      "isReView": "0",
      "ViewPoint": ""
    }
  ]
}
```