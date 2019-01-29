## 查询施工进度填报

> 用于查询历史施工进度填报

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/getPlanProgressInfo `

### 2. 请求参数

body:

| **参数**                | **数据类型** |  是否必须  | 描述     |
| ------------------------- | :--------: | :--: | ------------------------------------------------------------ |
| **userId**    | **String** |  Y   | 用户ID（填报人ID）                                           |
| **Projectid** | **String** |  Y   | 项目ID(审核人)                                               |

示例:

``` json
{
  "Projectid": "61",
  "userId": "496"
}
```
### 3. 返回参数

| 字段           | 字段类型 | 字段说明             |
| -------------- | :------: | -------------------- |
| **Code**       |  string  | 0：成功 ；其他：失败 |
| **CodeMsg**    |  String  | 失败时原因信息       |
| **LogID**      |  String  | 施工进度填报ID       |
| **Taskid**     |  String  | 计划ID               |
| **RstartDate** |  String  | 实际开始时间         |
| **REnddate**   |  String  | 实际截止时间         |
| **Pro**        |  String  | 完成进度             |
| **note**       |  String  | 备注                 |
| **adddate**    |  String  | 提交时间             |
| **Guid**       |  String  | 关联构件ID           |
| **FileLists**  |  Array   | 附件列表             |

返回示例：
```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": [
    {
      "LogID": 1094,
      "Taskid": "b51d7314-68ff-4083-a734-050d4db74475",
      "RstartDate": "2018/11/28 0:00:00",
      "REnddate": "2018/11/28 0:00:00",
      "DelayExplain": "",
      "StopExplain": "",
      "Pro": 20,
      "note": "",
      "adder": null,
      "adddate": "2018/11/28 18:00:41",
      "Status": 1,
      "ChangePro": 0,
      "ProjectID": 61,
      "Guid": "599_662037",
      "FileLists": []
    }
  ]
}
```