## 查询危险源监控跟踪历史列表

> 用于查询危险源监控跟踪历史列表

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/GetHazardMonitoringTrackingHistoryList`

### 2. 请求参数

body:

| 字段           | 字段类型 | 必填 | 字段说明                                                     |
| -------------- | :------: | :--: | ------------------------------------------------------------ |
| **projectId**  |  String  |  Y   | 项目ID                                                       |
| **userid**     |  String  |  Y   | 用户ID                                                       |
| **keyword**    |  String  |  N   | 关键字                                                       |
| **hazardMTId** |          |      | 危险源监控跟踪ID(从[GetHazardMonitoringTrackingList](GetHazardMonitoringTrackingList.md)而来，`Hid`) |

示例:

```json
{
  "userid": "496",
  "projectId": "61",
  "keywords": "",
  "hazardMTId": "105"
}
```

### 3. 返回参数

| 字段        | 字段类型 | 字段说明             |
| ----------- | :------: | -------------------- |
| **Code**    |  string  | 0：成功 ；其他：失败 |
| **CodeMsg** |  String  | 失败时原因信息       |
| **Logid** | String | ID |
| **rq** | String | 跟踪时间 |
| **CheckUser** | String | 检查人 |
| **Mcount** | String | 隐患通知单数 |
| **Mid** | String | 隐患通知单ID，可用来查询通知单详情 |

返回示例：

```json
{
    "Code": 0, 
    "CodeMsg": "OK", 
    "Datas": {
        "Logid": "79", 
        "rq": "2018/9/19 14:29:34", 
        "CheckUser": "wang1", 
        "Mcount": "1", 
        "Mid": "91"
    }
}
```