## 获取进度差异分析报表 – 图表数据

> 用于进度差异分析报表 – 图表数据

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/GetScheduleVarianceAnalysisCharts`

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

| 字段          | 字段类型 | 字段说明                     |
| ------------- | :------: | ---------------------------- |
| **Code**      |  string  | 0：成功 ；其他：失败         |
| **CodeMsg**   |  String  | 失败时原因信息               |
| **TaskState** |  String  | 任务状态（提前完工，未完工） |
| **TaskCount** |  String  | 任务数（可用来计算占比）     |

返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": [
    {
      "TaskState": "提前完工",
      "TaskCount": "176"
    }
  ]
}
```