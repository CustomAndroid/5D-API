## 获取安全整改通知单审核流程列表

> 用于获取安全整改通知单审核流程列表

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/GetSafetyRectificationNoticeProcess`

### 2. 请求参数

body:

| 字段          | 字段类型 | 必填 | 字段说明         |
| ------------- | :------: | :--: | ---------------- |
| **ProjectID** |  String  |  Y   | 项目ID           |
| **userId**    |  String  |  Y   | 用户ID           |
| **id**        |  String  |  Y   | 安全整改通知单ID |

示例:

```json
{
  "userid": "496",
  "projectid": "61",
  "id": "91"
}
```

### 3. 返回参数

| 字段        | 字段类型 | 字段说明             |
| ----------- | :------: | -------------------- |
| **Code**    |  string  | 0：成功 ；其他：失败 |
| **CodeMsg** |  String  | 失败时原因信息       |
| **Mid** | String | 整改通知单ID |
| **Lid** | String | 流程ID |
| **SenderId** | String | 上一流程审核人ID |
| **SendDate** | String | 上一流程审时间 |
| **ExecuteId** | String | 此次流程审核人 |
| **ExecuteDate** | String | 此次流程审核时间 |
| **Attitude** | String | 处理意见 |
| **Step** | String | 审核步骤 |
| **treat** | String | 处理结果 |
| **Status** | String | 状态 |
| **Note** | String | 备注 |

返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": [
    {
      "Lid": "106",
      "Mid": "91",
      "SenderId": "495",
      "SendDate": "2018/9/19 14:32:50",
      "ExecuteId": "498",
      "ExecuteDate": "2018/9/19 14:34:27",
      "Attitude": "同意",
      "Step": "1",
      "treat": "同意",
      "Status": "2",
      "Note": ""
    },
    {
      "Lid": "107",
      "Mid": "91",
      "SenderId": "498",
      "SendDate": "2018/9/19 14:32:50",
      "ExecuteId": "499",
      "ExecuteDate": "2018/9/19 14:35:42",
      "Attitude": "同意",
      "Step": "1",
      "treat": "同意",
      "Status": "2",
      "Note": ""
    },
    {
      "Lid": "108",
      "Mid": "91",
      "SenderId": "499",
      "SendDate": "2018/9/19 14:32:50",
      "ExecuteId": "495",
      "ExecuteDate": "2018/9/19 14:35:59",
      "Attitude": "同意",
      "Step": "1",
      "treat": "同意",
      "Status": "2",
      "Note": ""
    }
  ]
}
```